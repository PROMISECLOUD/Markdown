# AUTHENTICATION

Authenticating users in Payee solutions involves multiple layers of security to ensure that only legitimate users can access the system and perform transactions. All requests must be made over HTTPS and authenticated over standard HTTP basic authentication. Here’s a step-by-step outline of a robust authentication process for a Payee solutions:

### **1.** User Registration 

+ **Personal Information Collection:** Payee Solutions collect essential information such as name, email address, phone number, and government-issued identification. 
+ **Email and Phone Verification:** Payee Solutions sends a verification code to the user’s email or phone number to confirm their contact details.

### **2.** Multi-Factor Authentication (MFA)

+ **Password:** Require users to create a strong password that meets complexity requirements.
+ **One-Time Password (OTP):** Send an OTP via SMS, email, or an authenticator app that the user must enter to complete the login process.
+ **Biometric Verification:** Use fingerprint, facial recognition, or other biometric methods as an additional authentication factor.

### 3. Device Authentication

+ **Device Registration:** Payee Solutions registers user devices by associating them with user accounts. This may involve sending a confirmation link or code to the user to verify the device.
+ **Device Fingerprinting:** Use device fingerprinting techniques to gather information about the user's device (such as IP address, browser type, and operating system) and create a unique device ID.

## Create API key

API keys can be created, viewed and managed in the Payee Solutions dashboard on the Settings > Developers > API keys screen.
```
caution !

An invalid, missing or expired api key will result in HTTP 401 Unauthorized responses.

They should not be in your client-side code or checked into your application's code or commit your API keys to git.
```


|Field|Type|Description|
|-----|------|------|
|Authorisation|Header|Basic Authorisation header containg Base64|
|Username|String|Your username for accessing the API|
|Password|String|Your password for accessing the API

## Refrences

[Confluece: Autorisation](https://efficientpromise.atlassian.net/wiki/spaces/PAYEE/pages/edit-v2/6455301)

[ChatGPT](https://chatgpt.com/c/9499ec8f-0d57-407c-a6fd-732c7ba1650e)

[Youtube](https://www.youtube.com/watch?v=ftOBvusMHjQ)