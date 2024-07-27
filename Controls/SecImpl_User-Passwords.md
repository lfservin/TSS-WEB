# {{site.TITLE_IMPL_USERPASSWD}}

## 1. General

1. User password MUST be compliant to the password policy at both registration as well as password change and password reset functions.
2. As long as not specified differently by the password policy, the following minimum requirements for user passwords MUST apply:
    - Length >= 8 characters,
    - consists of characters, digits and special characters,
    - not be identical with the username,
    - be masked on all HTML password fields,
    - not be logged or cached,
    - encrypted when transferred over insecure channels,
    - not transmitted in URLs and
    - stored as a salted secure hash, ideally with key stretching. This SHOULD b implemented with [bcrypt](https://en.wikipedia.org/wiki/Bcrypt), [scrypt](https://en.wikipedia.org/wiki/Scrypt), [PBKDF2](https://en.wikipedia.org/wiki/PBKDF2) or [Argon2](https://en.wikipedia.org/wiki/Argon2) algorithm.
3. Initial user passwords MUST be changed by the user at first login.
4. Standard passwords (= set by the vendor) MUST NOT be used and replaced by strong
individual passwords.

## 2. Password Change Functions

1. Users MUST be able to change their passwords.
2. Users SHOULD be indicated the strength of the current password choice when changing their passwords (using a password strength functions).
3. Users MUST confirm a new password with their current ones.
4. Users SHOULD be informed when their password has changed (e.g. via e-mail notification).

## 3. Password Forgot Functions

1. MUST implement the same level of security protections as the user authentication function (e.g. anti-automation).
2. MUST be authorized by the user with the same method that is used as second factor or (in case no second factor is used) for user identification (e.g. e-mail address). Ideally, by using a One Time Token (OTT) with limited validity sent as a second factor (e.g. to the registered user e-mail address or mobile phone).
3. MUST not affect the state of the user profile before password reset is completed.