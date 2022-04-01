Primary service offered by an [IdP](/knowledge/LIP/IdP)

Authentication validates that the user is who they say they are. This is usually done through **something you know** and/or **something you have** and/or **something you are**.

- Something you know is a password, or your mother's maiden name, or your best friend when you were growing up.
- Something you have is a **Yubikey** or similar one time password ([OTP](/knowledge/LIP/OTP)) generating device
- Something you are is like the fingerprint sensor in your MacBook keyboard or an eye sensor or **FaceID**

These are sometimes used on their own or in combination with others. When you hear the term [2FA or MFA](/knowledge/LIP/MFA), they mean Two Factor Authentication and Multi Factor Authentication. So they use two or more factors: a password and [OTP](/knowledge/LIP/OTP) or **FaceID**. 

Authentication typically provides minimal to no information about whether that user or machine is authorized to use a particular resource, but the authentication information will be used by the authentication systems to determine access levels. 

The actual implementation of Authentication may use one of many different authentication protocols:

![Authentication Protocols](/knowledge/LIP/protocols/Authentication Protocols)