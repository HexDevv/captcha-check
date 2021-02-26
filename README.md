# captcha-check
> A module to easily integrate reCAPTCHA and other services

<details>
  <summary><strong>Changelog</strong></summary>
 
 ### 1.0.0 - captcha-check was created! 🎉
 - Added reCAPTCHAv2 & hCaptcha

</details>

# Usage
```js
const Captcha = require('captcha-check');

// Adding a captcha service. Captcha services are available in the readme.md
const captcha = new Captcha({service:'recaptcha', secretkey:process.env.SECRET});

// returns true|false. ipAddress optional
captcha.check(res.captchaResponse, ipAddress);

// returns an array. {success: true|false, timestamp: timestamp (ISO format yyyy-MM-dd'T'HH:mm:ssZZ), hostname: string}
captcha.detailedCheck(res.captchaResponse, ipAddress);
```

# Supported Captcha services:

| Captcha Service   | Tag       | Notes |
|-------------------|-----------|-------|
| [reCAPTCHAv2](https://developers.google.com/recaptcha/docs/display)       | `recaptcha` |       |
| [reCAPTCHAv2 Invis](https://developers.google.com/recaptcha/docs/invisible) | `recaptcha` |       |
| [hCaptcha](https://www.hcaptcha.com/)          | `hcaptcha`  |       |
