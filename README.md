# Sample Repo Demonstrating LWC OSS Styling Issues

This repo is an attempt to use [Bulma](https://bulma.io) to style a LWC OSS app.
The sample app is supposed to render a [basic navbar example](https://bulma.io/documentation/components/navbar/#basic-navbar).

By default, the app renders the right content based on subsets of Bulma built from SASS. This works but requires manual config to generate CSS from SASS..

Two issues that can be reproduced by modifying `app.css`:

-   building with the original Bulma CSS file (`bulma-full.css`) will make the LWC compiler crash with a "Invalid definition of custom property "--columnGap"" message (unsupported CSS variables).
-   building with a modified version of Bulma (`bulma-no-vars.css`) without CSS variables will crash with a "RangeError: Maximum call stack size exceeded" message.
