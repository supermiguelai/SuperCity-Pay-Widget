# SuperCity-Pay-Widget
SuperCity Payment Form Widget
## Installation

1. Place CSS & JS files somewhere on webserver so they are publicly accessible
2. Attach CSS & JS files inside of `<head>` tag on your website
```html
<script src="<path_to_widget>/supercity-payment-form.js"></script>
<link rel="stylesheet" href="<path_to_widget>/supercity-payment-form.css">
```
3. Run following script to initialize the Payment Form Widget (all properties are required and can be configured based on your needs - it is meant to be the output of registration form that should act as input to this payment form)
```js
document.addEventListener('DOMContentLoaded', function () {
  if (window.initPaymentForm) {
    window.initPaymentForm({
      user: {
        fullName: 'John Doe',
        caseNumber: '#20240CM0490',
        address: {
          street: '1234 Elm Street',
          city: 'Springfield',
          state: 'Illinois',
          zipCode: '62704',
        },
        phoneNumber: '+15550101234',
        email: 'test@example.com',
      },
      service: {
        title: 'Mediation Service',
        basePrice: 300,
        cardProcessingFeePercentage: 2.5,
        convenienceFeeAmount: 2,
        superCityPayFeeAmount: 1,
      },
      namespace: 'el-paso',
    });
  }
});
```
