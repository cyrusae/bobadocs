---
sidebar_position: 3
---

# Install BobaEditor

\[[code](https://github.com/essential-randomness/boba-editor), [demo](https://bobaeditor.netlify.app/?path=/story/editor-preview--simple-editor)]

BobaEditor is BobaBoard's own extension of the [QuillJS text editor](https://quilljs.com/), and is responsible for anything related to **text formatting** and **embeds** (both in "edit" and "display" mode).

## Install Instructions

In a terminal, run the following commands:

```bash
# Clone the codebase from github
git clone https://github.com/essential-randomness/boba-editor.git
# Enter the codebase directory
cd boba-editor
# Install all necessary code
yarn install
```

## Development Instructions

In a terminal, run the following command:

```bash
yarn run storybook
```

You should now have a DevServer running at [http://localhost:6006](http://localhost:6006) that will look something like [the online demo](https://bobaeditor.netlify.app/).

:::tip
If new code dependencies have been added, you might need to re-run `yarn install`. If the above command is giving you problems, give it a try!
:::

## Developing for Embeds

Embeds that rely on [iFramely](https://github.com/itteco/iframely) won't work out of the box. If you're developing for embeds, you have two options:

### Option 1: Connect to the BobaBoard embeds service (Recommended)

Given that the embeds service won't accept requests from localhost for security reasons, you will need to install an "Allow CORS extension" ([example for Chrome](https://chrome.google.com/webstore/detail/allow-cors-access-control/lhobafahddgcelffkeicbaginigeejlf?hl=en)). Once you allow [CORS](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing) in your browser window, embeds should automatically start working.

### Option 2: Run iFramely on your own machine

:::caution
You shouldn't need to do this, unless you're fiddling with iFramely's setup.
:::

You can run storybook pointing to a local instance of iFramely by using the `yarn run storybook:local-embeds` command. To run your own iFramely you can use the instructions [here](https://iframely.com/docs/host). You will also likely need BobaBoard's iframely config as a started config. You can ask the webmaster for a copy of this file.
