# Quill icons

- Repo: https://github.com/deriv-com/quill-icons
- Storybook: https://quill-icons.pages.dev/
- Quill park : https://quill-icons-park.pages.dev/
- Npm package: https://www.npmjs.com/package/@deriv/quill-icons

```sh
    npm i @deriv/quill-icons 
```

## Installation

Install quill-design from this repo https://github.com/deriv-com/quill-icons. 
  
**Install your dependencies**

``` sh
    npm ci
```

## Environment Variables

**Setup .env file**

Configure the environment variables of the platform with these:

``` sh
    FIGMA_TOKEN=YOUR_FIGMA_TOKEN
    FILE_ID=XegjSl9fWXH2O7Mxo0Ctie
    ICONS_PAGE=deriv-icons
```

This file consists of 3 variables

1. **FIGMA_TOKEN:** We can generate our own figma token from our figma account. 

      Go to figma > Menu (from top left corner) >  Help & Account >  Account setting > Personal access token then generate access token and copy paste in your env file.

2. **FILE_ID:** File id which can be seen from any figma url(each figma will have different file id)

      eg: `https://www.figma.com/file/XegjSl9fWXH2O7Mxo0Ctie/Core-system-(Copy)?type=design&node-id=0-1&mode=design&t=NgnX6TdmKTqX8kbE-0`

3. **ICONS_PAGE:** Icons page can be any name we give, here we are using deri-icons.

## Export

The main idea of quill-icons project is to export svg icons/files from figma as a package that can be used in various apps. Quill icons are exported in 3 ways

- **Svg**(export as normal svg - can be found under svg folder of this repo)
- **React** (export svg as react components - can be found under src/react)
- **Stories** (story books are for visual representation - `https://quill-icons.pages.dev/`, here we can search icons and also find code for how to use in our apps)


We are using `outputters` from @figma-export to achieve the above exports.

Like, 

- `@figma-export/output-components-as-svg` to export svg
- `@figma-export/output-components-as-svgr`  to export svg as react components
- custom outputter for stories (can check under scripts > outputters > stories)

By running the following command all 3 exports will be built. 
                   
## Figma config file

Design team is creating icon collections exclusive for the quill design system [here]([https://www.figma.com/developers/api#authentication](https://www.figma.com/file/c24yCkzAgS5Fv1x0QuEYxq/Quill-icons-for-FE?type=design&node-id=0-1&mode=design&t=0R38TqbkYiOo84GT-0)) 

This the figma file id `c24yCkzAgS5Fv1x0QuEYxq` which is used as the default config file. 
As we can see few categories in the above figma like flags, currencies, markets, illustrative, trade types and few others yet to be added. So whenever a new icon is added to this figma we can run and export the project and a new version of the quill-icon package will be created. 

**Create new category**

To create a new category which is not present in this file(`c24yCkzAgS5Fv1x0QuEYxq`) we need to add a new figma config file. 
we can add it under scripts

                `<categoryName>.figma.config.ts` 

(eg: logos -> `logo.figma.config.ts`)

## Storybook

We can build the storybooks by running the command and check the icons 

```sh
   npm run storybook
```        



                   
