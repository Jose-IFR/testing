<div id="top"></div>

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

### Installation

- Use the following VTEX CLI command to install the service in your store
  ```
  vtex install vtex.paypal-utils
  ```

### Usage

1. Setup a cloud cron job scheduler, we suggest **_Google Cloud Scheduler_**, however you can use whichever you decide.

   ![Google Scheduler Screen][scheduler-screenshot]

2. Once you have your cron scheduler ready to be configured, setup a request to activate the process every N minutes.

   - URL: `https://{{account}}.myvtex.com/_v/payPal2?cancel=true`
   - Frequency: `*/10****`

  <blockquote>
    <p dir="auto">
      <g-emoji class="g-emoji" alias="warning" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/26a0.png">⚠️  </g-emoji>
      <strong>The recommened frequency for this unix cron process is between 5 to 10 minutes, depending on the amount of Paypal orders recived</strong>
    </p>
  </blockquote>

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ARQUITECTURE -->

## Arquitecture
1. The policies in the manifest.json
![Manifest][manifest-screenshot]

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- LICENSE -->

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->


<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments

- []()
- []()
- []()

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[vtexio-shield]: https://img.shields.io/badge/VTEX-%20IO-%23ff69b4
[maintained-shield]: https://img.shields.io/badge/MANTAINED-%20NO-%23ff0000
[arquitecture-screenshot]: https://user-images.githubusercontent.com/18706156/77381360-72489680-6d5c-11ea-9da8-f4f03b6c5f4c.jpg
[scheduler-screenshot]: https://user-images.githubusercontent.com/65255533/110838782-7c62ee00-8268-11eb-8a41-71cb5ae1927b.png
[manifest-screenshot]: /blob/code.png