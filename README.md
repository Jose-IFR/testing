<div id="top"></div>

![VTEX][vtexio-shield]
![Mantained][maintained-shield]

# NOT MANTAINED

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h3 align="center">Paypal Service utils</h3>
  <p align="center">The objective of this app is to cancel Paypal standing orders every N amount of time configured.
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
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
      <a href="#customization">Customization</a>
    </li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

<!-- [![Product Name Screen Shot][product-screenshot]](https://example.com) -->

This code is provided as is, use it and customize it at your risk and convenience.

The objective of this app is to manage the cancelation of Paypal standing orders every N amount of time configured.

![Service Example Architecture](https://user-images.githubusercontent.com/18706156/77381360-72489680-6d5c-11ea-9da8-f4f03b6c5f4c.jpg)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

### Install service in your store using VTEX CLI

1. ```sh
   vtex install vtex.paypal-utils
   ```
2. Get a cloud cron job scheduler, we suggest **_Google Cloud Scheduler_**, however you can use whichever you decide.

3. Once you have your cron scheduler in place, send a request to activate the process every N minutes

<blockquote>
  <p dir="auto">
    <g-emoji class="g-emoji" alias="warning" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/26a0.png">⚠️  </g-emoji>
    <strong>The recommened cyle to run the process is between 5 to 10 minutes, depending on the amount of Paypal orders recived</strong>
  </p>
</blockquote>

<p align="right">(<a href="#top">back to top</a>)</p>

### Recomendation

Use a a unix cron to do so like this for each 5 to 10 minutes depending on the volume of PayPal orders recived

`*/10 * * * *`

<!-- USAGE EXAMPLES -->

## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ROADMAP -->

## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
  - [ ] Nested Feature

See the [open issues](https://github.com/Jose-IFR/testing/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

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

## Contact

Your Name - [@twitter_handle](https://twitter.com/twitter_handle) - email@email_client.com

Project Link: [https://github.com/Jose-IFR/repo_name](https://github.com/Jose-IFR/repo_name)

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
[maintained-shield]: https://img.shields.io/badge/Mantained-%20NO-%23ff0000
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/joseibarrafloresramirez/
[product-screenshot]: images/screenshot.png
