# Exception Activity

## Description

This is an implementation of BankAccounts wave one. Our task today will be to change the behavior of `Bank::Account#withdraw`.

As things stand, when a withdrawal would make the account balance go negative, the program `puts` a message to the screen and returns the un-modified balance. Instead, we should raise an exception.

Work will proceed in 3 stages:

1. Change the tests for `Bank::Account#withdraw` to expect an exception rather than a `puts`
1. Define a new exception, `InsufficientFundsError`, in a new file `lib/insufficient_funds_error.rb`. `InsufficientFundsError` should inherit from `StandardError`.
1. Modify the `#withdraw` method to raise the exception rather than calling `puts`
