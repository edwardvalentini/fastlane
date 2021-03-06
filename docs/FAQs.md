FAQs
=====

### I'm getting an SSL error

If your output contains something like

```
SSL_connect returned=1 errno=0 state=SSLv3 read server certificate B: certificate verify failed
```

that usually means you are using an outdated version of OpenSSL. Make sure to install the latest one using [homebrew](http://brew.sh/).

```
brew update && brew upgrade openssl
```

### Error when running `fastlane` with Jenkins

This is usually caused when running Jenkins as its own user. While this is possible, you'll have to take care of creating a temporary Keychain, filling it and then using it when building your application. 

For more information about the recommended setup with Jenkins open the [Jenkins Guide](https://github.com/KrauseFx/fastlane/blob/master/docs/Jenkins.md).
