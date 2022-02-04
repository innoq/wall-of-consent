# Wall of Consent

[![npm version](https://badge.fury.io/js/wall-of-consent.svg)](https://badge.fury.io/js/wall-of-consent)

Ask user for consent before embedding scripts from third parties.

This package contains the custom element `<wall-of-consent />`. In order to work, it expects the following markup structure:

```html
<wall-of-consent>
  <template>
    Third party code goes here
  </template>
  <input type="checkbox"> Do you agree ...?
</wall-of-consent>    
```

### Usage

Install this npm package and import the code into your JavaScript:

```
npm install wall-of-consent --save-dev
```

```JavaScript
import "wall-of-consent";
```

### Example

```html
<wall-of-consent>
    <template>
        <blockquote class="twitter-tweet" data-conversation="none" data-lang="en" data-dnt="true"><p lang="en" dir="ltr">Doge spelled backwards is Egod</p>&mdash; Elon Musk (@elonmusk) <a href="https://twitter.com/elonmusk/status/1368058884837928970?ref_src=twsrc%5Etfw">March 6, 2021</a></blockquote>
        <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
    </template>
    <p data-hide-if-consent>Would you like to embed code and cookies from twitter directly into this page?</p>
    <label>
        <input type="checkbox" />
        Show tweets
    </label>
</wall-of-consent>
```
