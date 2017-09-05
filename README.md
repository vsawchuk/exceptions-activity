# Exception Activity

## Description

This is an incomplete implementation of a system that tracks Bank Account transactions.
The code provided has the following qualities:
- There is one class called `Account` in the module `Bank`
- Each `Account` has an ID and a balance
- Each `Account` can `withdraw` and `deposit` a given amount, which affects the balance.

Our task today will be to change the behavior of the provided `Bank::Account#withdraw`.

As things stand, when a withdrawal would make the account balance go negative, the program `puts` a message to the screen and returns the un-modified balance. Instead, we should raise an exception.

Work will proceed in 3 stages:

1. Change the tests for `Bank::Account#withdraw` to expect an exception rather than a `puts`
1. Define a new exception, `InsufficientFundsError`, in a new file `lib/insufficient_funds_error.rb`. `InsufficientFundsError` should inherit from `StandardError`.
1. Modify the `#withdraw` method to raise the exception rather than calling `puts`
