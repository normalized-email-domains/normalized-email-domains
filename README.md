# Normalized Email Domains

I had enough of projects that just lowercase the whole email, throw out all dots, dashed, and everything after a plus sign, and so one.

This project is inspired by https://github.com/disposable-email-domains/disposable-email-domains.

## Data format

You can find a JSON schema for the data [here](./data.schema.json).

```json
{
  "$schema": "https://github.com/normalized-email-domains/normalized-email-domains/data.schema.json",
  "primaryDomain": "gmail.com",
  "features": [
    {
        "feature": "case-insensitive-localpart",
        "source": [ "https://www.businessinsider.com/guides/tech/are-gmail-addresses-case-sensitive" ]
    },
    {
        "feature": "dots-ignored",
        "source": [ "https://support.google.com/mail/answer/7436150?hl=en" ]
    },
    {
        "feature": "subaddress-support",
        "source": [ "https://support.google.com/a/users/answer/9282734?hl=en#email-address-variation" ]
    }
  ],
  "aliases": [ "googlemail.com" ]
}
```

## Features Explained

### Subaddress support (`subaddress-support`)

The part after the "+" symbol in an email address is typically referred to as a subaddress or a sub-identifier. It is also sometimes called a username extension, alias, or tag.

Subaddresses can be used to create unique identifiers for different purposes or to filter and organize incoming email. For example, if your email address is "johndoe@gmail.com", you could use a subaddress like "johndoe+newsletter@gmail.com" when subscribing to newsletters, or "johndoe+work@gmail.com" when communicating with work contacts. This way, you can easily filter and manage incoming email based on the subaddress used.
