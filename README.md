# AEM Webpack Example

This project demonstrates a proven practice for setting up Webpack in AEM. It provides a straightforward Webpack configuration that supports Babel, JavaScript and CSS linting, and JavaScript testing. It is part of the setup [Infield Digital](http://www.infielddigital.com/) introduced to some major AEM customers.

## Why Webpack in AEM?

AEM might be the best system for content and user experience management. It provides reliable tools that power [some](http://store.nike.com/) [of](https://aws.amazon.com/) [the](https://www.chase.com/) [biggest](https://www.salesforce.com/) websites and that Java developers enjoy working with.

However, your front-end developers are probably not be happy with it and waste precious time. Why? AEM's out-of-the-box tools can't keep up with the rapid advances in the front-end world.

![Front-end development in AEM](https://i.imgur.com/vKwoLvU.jpg)

**Webpack in AEM improves front-end development because...**

- It allows using the latest JavaScript standards _without_ breaking clientlibs and AEM's built-in YUI compressor.
- It promotes modular and reusable code. You can import modules, variables and files using JavaScript and tie it to an AEM component. This results in code that's easier to maintain, which saves time and _$$$_.
- It can be extended easily and supports the integration of [~500.000](http://www.modulecounts.com/) npm modules.
- It can automatically prefix CSS for better cross-browser compatibility, ensure consistent code style, and automate most tasks you can think of.
- It even allows writing tests for JavaScript.

**Let's make AEM fun for everyone.**

![Make AEM fun again](https://i.imgur.com/t37OlGq.jpg)

## Integrate Webpack into AEM

The structure of this project mirrors Adobe's [Project Archetype](https://github.com/Adobe-Marketing-Cloud/aem-project-archetype/tree/master/src/main/archetype). To get started, you can either [set up a new project](https://github.com/Adobe-Marketing-Cloud/aem-project-archetype) using the archetype, or you use your existing project. Then...

Here's a step-by-step summary. Each step links to a folder containing a **README** file with more instructions. Make sure you read those for detailed instructions of each aspect.

1. [Copy the example Webpack folder](ui.apps/src/main) to `ui.apps/src/main`.
2. [Copy .babelrc, .eslintrc.js and .stylelintrc](ui.apps/src/main) to `ui.apps/src/main`.
3. [Extend your project's pom.xml](ui.apps).

This is already enough to run the project's Maven build and Webpack. Try it now! Then you want to modify a few more things:

4. [Use the generated files on your page](ui.apps/src/main/content/jcr_root/etc/designs/__appsFolderName__/clientlib-components), for example by including them in a clientlib.
5. [Adjust filters](ui.apps/src/main/content/META-INF/vault) in `ui.apps/src/main/content/META-INF/vault`.
6. [Add files generated by Webpack to .gitignore](ui.apps/src/main).

## Toolbox

AEM Webpack Example supports the following tools out-of-the-box:

- Maven integration using [frontend-maven-plugin](https://github.com/eirslett/frontend-maven-plugin).
- Webpack.
- CSS/SCSS.
- Babel. JavaScript compilation using Babel's recommended [env preset](http://babeljs.io/docs/plugins/preset-env/).
- ESLint. Linting for JavaScript.
- Stylelint. Linting for CSS/SCSS.
- Autoprefixer. Prefixes CSS/SCSS to improve cross-browser compatibility.
- Jest. Testing for JavaScript.

## Demo

Video summary:

* Automatically watch to JavaScript and SCSS changes using script `npm run build:watch`
* See what happens if CSS violates a Stylelint rule
* See what Autoprefixer does to your CSS

[![Webpack in use](http://infielddigital.com/shared/aem-webpack-example-demo-thumbnail.jpg)](http://infielddigital.com/shared/aem-webpack-example-demo.mov)

## Tips

- Speed up development using [AEM Front](https://www.npmjs.com/package/aem-front). If used, Webpack can be run from the [webpack](ui.apps/src/main/webpack) folder. There's no need to run Maven every time a JavaScript or CSS change should be deployed to a local AEM instance. Instead, use Webpack's watch tasks in combination witih AEM Front.
- If you or your company are looking for AEM or front-end experts, meet [Infield Digital](http://www.infielddigital.com/).
