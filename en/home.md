<hr>

[![Midtrans Logo](/asset/image/main/midtrans-logo.svg ':size=220')](https://midtrans.com)<hr>

Midtrans helps your business to easily accept, disburse payments, and many more in an automated manner. Get to know the technical details or see our products’ documentations here.

<!-- TODO: add more image for each product so it doesn't look to plain? -->
## Accept Online Payments on Your Website and App {docsify-ignore}

<div class="my-card">

#### [Use Midtrans Checkout Page (SNAP Checkout) &#187;](/en/snap/overview.md#overview)
Securely accept payment on your web and app with few simple steps! Your customer will be presented with a sleek, mobile-friendly interface to do payment with, straight inside your web and app in form of a pop-up dialogue box (or redirected to Midtrans' URL if you choose to). With a single integration, SNAP’s user interface allows you to accept payment via Midtrans's' [available payment methods](https://midtrans.com/payments).

<br> <!-- TODO: use better CORS proxy, cors-anywhere is limited per referrer domain  -->
<p style="text-align: center;">
  <button onclick="
  event.target.innerText = `Processing...`;
  fetch(`https://cors-anywhere.herokuapp.com/https://midtrans.com/api/request_snap_token`)
    .then(res=>res.json())
    .then(res=>{
      let snapToken = res.token;
      snap.pay(snapToken,{
        onSuccess: function(res){ console.log('Snap result:',res) },
        onPending: function(res){ console.log('Snap result:',res) },
        onError: function(res){ console.log('Snap result:',res) },
      });
    })
    .catch( e=>{ console.error(e); window.open('https://demo.midtrans.com', '_blank'); } )
    .finally( e=>{ event.target.innerText = `Pay with Snap &#9099;` })
  " class="my-btn">Try SNAP Payment Interface &#9099;</button>
</p>
<div style="text-align: center;">

<sup>[Or test directly at our integration implementation!](/en/snap/interactive-demo.md)</sup>
</div>
</div>

<div class="my-card">

#### [Mobile SDK &#187;](https://mobile-docs.midtrans.com)
Midtrans checkout page for native mobile platforms - easily embed our Android and iOS Mobile SDK within your app to start accepting payments natively within the app. We provide the drop-in User Interface to accept payment using multiple methods supported by Midtrans. Check out this [video](https://www.youtube.com/watch?v=EefsTMXCscg) for the default SDK example.
</div>

<div class="my-card">

#### [Build Your Own Checkout Page (Core API) &#187;](/en/core-api/overview.md)
Need to customize the payment flow or user interface to fit your business’ specific needs? We have Core API for your web, app, point of sales, IoT or any internet-capable device which allows you to accept payments directly in your own checkout page. Core API uses the familiar REST API standard with JSON-based payload.
</div>

<div class="my-card">

#### [Use CMS Payment Plugin &#187;](/en/snap/with-plugins.md)
Not a developer, or already using e-commerce CMS? Integrate to Midtrans via your choice of CMS plugin in a few simple clicks. 
</div>

<div class="my-card">

#### [Create Invoice via Payment Link &#187;](/en/payment-link/overview.md)
Whether you need to invoice your customers or want to receive payments without having a website, you can do it with Midtrans - as easy as sharing a link that redirects your customers to Midtrans's payment page. No technical integration is required; create payment links in just a few clicks via our dashboard with customizable payment details.
</div>

## Pay Out / Disburse Fund {docsify-ignore}

<div class="my-card">

#### [Pay Out via Iris Disbursement System &#187;](https://iris-docs.midtrans.com/)

Transfer funds to your partners, sellers, customers, vendors or any third parties with our Iris Disbursement system. Whether you are a marketplace needing to disburse money to sellers, or business doing payrolls transfers to your employees - all of your payout needs can be catered by Iris. Iris supports disbursing money to Gopay accounts or any kind of bank accounts in Indonesia.
</div>

## Misc {docsify-ignore}

<!-- TODO: write this page -->
<div class="my-card">

<!-- #### [Integrate Payment to POS &#187;](/en/pos/overview.md) -->
#### [Integrate Payment to POS &#187;](#accept-payment-on-point-of-sales-vending-machine-iot-devices-etc)
</div>

<br> <br>


# Integrate based on Your Business Use Cases {docsify-ignore}

Here are some popular use cases that may help you choose:

#### Accept payment on your e-commerce web, app

Accept payment from your customer straight within your website/app via Credit and Debit Cards, Bank Transfer, Direct Debit, E-Wallet, [and more](https://midtrans.com/payments). Use [SNAP's beautiful interface](/en/snap/overview.md) or [Customizable Core API](/en/core-api/overview.md) to enable your web and app to accept payment securely in a few simple steps.

#### Subscription / Recurring Service

Accept recurring payments automatically from your customer for subscriptions, membership billing, repeat item purchase or billing with flexible interval period according to your business needs. Your customer will be automatically charged recurringly without the need to ask your customer to make payments each time. Recurring payment is available in [SNAP](/en/snap/advanced-feature.md#recurring-subscription-card-transaction) and [Core API](/en/core-api/advanced-features.md#recurringone-click-transaction) integration. \**Recurring is only available for certain payment channels*.

#### Sending payment invoices via Email, Link, Whatsapp, Instagram, Social Media, Messaging App, etc
<!-- <TODO: elaborate payment link or maybe also selly?> -->
Invoice and accept payments from your customers via [Payment Link](/en/payment-link/overview.md). You will only need to go to Midtrans Dashboard, generate a payment link, and then share the link to your customers via your favorite messaging app. Midtrans Payment Link is a perfect fit for social commerce seller, freelancer, service provider, hospitality and travel business, or businesses which need to quickly invoice specific customers, etc.

#### Accept payment on Point of Sales, Vending Machine, or IoT devices

O2O concept or non-conventional web/app platform such as vending machine, TV box, IoT, point of sales, etc. Integrate via [Midtrans Core API](/en/core-api/overview.md) to start accepting payment on the device. With Core API, devices can easily be integrated via API call/command as the communication medium. For GoPay integration to Point of Sales, see our [PoS GoPay Integration Guide](https://midtrans-advanced-faq.netlify.com/#/partner-gopay-pos).

#### Payout to sellers, buyers, or vendors / service providers.
<!-- <TODO: elaborate iris> -->
Whether you are an e-commerce marketplace/platform (whether it is B2C, B2B, or any other model) that connect services/goods seller to buyer, or businesses working with many vendors - you will need a solution to easily bulk payout or disburse funds to multiple bank and e-wallet accounts. We got you covered with our easy-to-use, automated [Fund Disbursement System: Iris](https://midtrans.com/iris).

<!-- < TODO:Add More Use Case> -->
<!-- Case Topup -->

# Not a Technical Person? {docsify-ignore}

<!-- <TODO: elaborate plugin, payment link, or snap plugin for non-dev reader> -->

Not familiar with programming, technical integration, and all the complexity? We have a way for you to accept payments with no coding needed:

- Simplest way to accept payment via Midtrans without a website or technical resources is via [**Payment Link**](/en/payment-link/overview.md). You will only need to login via browser to Midtrans Dashboard, generate payment link, and then share the link to your customers.

- Did you know you can utilize ready to use Content Management System (CMS) to create an online store? Are you familiar with CMS like: **Wordpress - Woocommerce, Magento, Prestashop, Opencart, WHMCS**, etc. ? You can setup those CMS online without any complex programming needed, and then install Midtrans plugin/extension to start accepting payment right away! Check out [Midtrans's list of supported CMS plugin/extension](/en/snap/with-plugins.md).

- Did you know there are also 3rd party E-commerce solution like **Shopify, Sirclo, Jejualan**, etc. that are ready to use, easy to use, user-friendly, and require very minimal setup? Midtrans is already integrated to many 3rd party E-commerce solutions available to use right away. Check out [Midtrans's list of supported 3rd party E-commerce platform](/en/snap/platform/overview.md).
