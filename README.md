### How to add Storybook to a Typescript CRA project

1. Run `npx create-react-app [project-name] --template typescript`
2. Run `npx -p @storybook/cli sb init`
3. In `.storybook/main.js` update line 2 to look for .tsx files instead of .js. It should look like this:
```js
module.exports = {
  stories: ['../src/**/*.stories.tsx'],
  addons: [
    '@storybook/preset-create-react-app',
    '@storybook/addon-actions',
    '@storybook/addon-links',
  ],
};
```
4. Running `yarn storybook` should now show any `*.stories.tsx` files you've created!


### Docs to reference

[Developing Components in Isolation - create-react-app.dev](https://create-react-app.dev/docs/developing-components-in-isolation)

[TypeScript Config - storybook.js.org](https://storybook.js.org/docs/configurations/typescript-config/)

[Writing Stories - storybook.js.org](https://storybook.js.org/docs/basics/writing-stories/)
