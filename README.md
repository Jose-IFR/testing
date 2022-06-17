<div id="top"></div>

# <g-emoji class="g-emoji" alias="warning" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/26a0.png">⚠️</g-emoji> IMPORTANT <g-emoji class="g-emoji" alias="warning" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/26a0.png">⚠️  </g-emoji>

* This application is not maintained by the VTEX team 

<hr />

# Paypal Service utils

![vtex-version][vtexio-shield]
![maintained-status][maintained-shield]

<!-- TABLE OF CONTENTS -->
<details>
  <summary><h3>Table of Contents</h3></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#usage">Usage</a></li>
      </ul>
    </li>
    <li>
      <a href="#arquitecture">Architecture</a>
    </li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

This code is provided as is, use it and customize it at your risk and convenience.

The objective of this app is to manage the cancelation of Paypal incomplete orders with a custom frequency.

![Service Example Architecture][arquitecture-screenshot]

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

### App installation

- Use the following VTEX CLI command to install the service in your store  
`vtex install vtex.paypal-utils`

### Usage

1. Setup a cron job to request the activation of the app with a suggested frequency of 5 to 10 mins, depending on your store's order volume.

   - URL: `https://{{account}}.myvtex.com/_v/payPal2?cancel=true`
   
   - Frequency: `*/10****`  


  <g-emoji class="g-emoji" alias="warning" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/26a0.png">⚠️ </g-emoji>
  <strong>If you don't have a dedicated server to run your cron jobs, then we suggest using **_Google Cloud Scheduler_**, however you can use the service of your choice.</strong></p></blockquote>

   ![Google Scheduler Screen][scheduler-screenshot]


  


<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ARQUITECTURE -->

## How does this app work?

1. ###  Policies in manifest.json
  
   The manifest.json file has specific access policies, in this specific case, we have the outbound for the vtex portal account.


<img src="https://user-images.githubusercontent.com/105675260/172765222-10483ca8-5f66-449d-8a33-984127a2e0aa.png" alt="drawing" width="600"/>

2. ### middlewares

- PayPal2.ts
- PayPalOrders.ts

3. ### clients

- PayPalUtils.ts

4. ### utils

- authToken.js
- cachedContext.ts
- seller.js
- statusError.ts
- tracing.js

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments

- Rodrigo Olivera

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[vtexio-shield]: https://img.shields.io/badge/VTEX-%20IO-%23ff69b4
[maintained-shield]: https://img.shields.io/badge/MANTAINED-%20NO-%23ff0000
[arquitecture-screenshot]: https://user-images.githubusercontent.com/18706156/77381360-72489680-6d5c-11ea-9da8-f4f03b6c5f4c.jpg
[scheduler-screenshot]: https://user-images.githubusercontent.com/65255533/110838782-7c62ee00-8268-11eb-8a41-71cb5ae1927b.png
[manifest-screenshot]: /blob/code.png
