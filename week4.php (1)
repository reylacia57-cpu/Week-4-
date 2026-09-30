<?php

trait Logger {
    public function logTransaction($message) {
        echo "[LOG]: " . $message . "<br>";
    }
}

class BankAccount {
    use Logger;

    private $balance;

    public function __construct($balance = 0) {
        $this->balance = $balance;
    }

    public function getBalance() {
        return $this->balance;
    }

    public function deposit($amount) {
        $this->balance += $amount;
        $this->logTransaction("Balance updated by +$amount");
    }

    public function withdraw($amount) {
        $this->balance -= $amount;
        $this->logTransaction("Withdrawal of $amount, new balance: " . $this->balance);
    }
}

$account = new BankAccount(1000);

echo "Initial balance: " . $account->getBalance() . "<br>";

$account->deposit(500);
$account->withdraw(400);

?>