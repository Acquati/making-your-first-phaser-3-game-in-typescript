![phaser3-parceljs-template](https://user-images.githubusercontent.com/2236153/71606463-37a0da80-2b2e-11ea-9b5f-5d26ccc84f91.png)

# Making Your First Phaser 3 Game in Typescript

Based on the tutorial [Making Your First Phaser 3 Game](http://phaser.io/tutorials/making-your-first-phaser-3-game/part1) and [Ourcade - Making Your First Phaser 3 Game in TypeScript](https://www.youtube.com/watch?v=Pq75oRBjtzs&list=PLumYWZ2t7CRvLU1E-n6VDiOdfEeRQSXPE&index=1).

This project uses [phaser3-typescript-parcel-template](https://github.com/ourcade/phaser3-typescript-parcel-template).

## Prerequisites

You'll need [Node.js](https://nodejs.org/en/) and [yarn](https://yarnpkg.com/).

## Getting Started

Clone this repository to your local machine:

```bash
git clone https://github.com/Acquati/ourcade-phaser-3-game-typescript.git
```

This will create a folder named `ourcade-phaser-3-game-typescript`. You can specify a different folder name like this:

```bash
git clone https://github.com/Acquati/ourcade-phaser-3-game-typescript.git my-folder-name
```

Go into your new project folder and install dependencies:

```bash
cd ourcade-phaser-3-game-typescript # or 'my-folder-name'
yarn install
```

Start development server:

```
yarn start
```

To create a production build:

```
yarn build
```

Production files will be placed in the `dist` folder. Then upload those files to a web server. 🎉

## Project Structure

```
    .
    ├── dist
    ├── node_modules
    ├── public
    ├── src
    │   ├── scenes
    │   │   ├── HelloWorldScene.ts
    │   ├── index.html
    │   ├── main.ts
    ├── package.json
```

The contents of this template is the basic [Making Your First Phaser 3 Game](http://phaser.io/tutorials/making-your-first-phaser-3-game/part1).

This template assumes you will want to organize your code into multiple files and use TypeScript.

TypeScript files are intended for the `src` folder. `main.ts` is the entry point referenced by `index.html`.

Other than that there is no opinion on how you should structure your project. There is a `scenes` folder in `src` where the `HelloWorldScene.ts` lives but you can do whatever you want.

## Static Assets

Any static assets like images or audio files should be placed in the `public` folder. It'll then be served at http://localhost:8000/images/my-image.png

Example `public` structure:

```
    public
    ├── images
    │   ├── my-image.png
    ├── music
    │   ├── ...
    ├── sfx
    │   ├── ...
```

They can then be loaded by Phaser with `this.image.load('my-image', 'images/my-image.png')`.

## TypeScript ESLint

This template uses a basic `typescript-eslint` set up for code linting.

It does not aim to be opinionated.

## Dev Server Port

You can change the dev server's port number by modifying the `start` script in `package.json`. We use Parcel's `-p` option to specify the port number.

The script looks like this:

```
parcel src/index.html -p 8000
```

Change 8000 to whatever you want.

## Other Notes

[parcel-plugin-clean-easy](https://github.com/lifuzhao100/parcel-plugin-clean-easy) is used to ensure only the latest files are in the `dist` folder. You can modify this behavior by changing `parcelCleanPaths` in `package.json`.

[parcel-plugin-static-files](https://github.com/elwin013/parcel-plugin-static-files-copy#readme) is used to copy static files from `public` into the output directory and serve it. You can add additional paths by modifying `staticFiles` in `package.json`.
