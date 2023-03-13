# Shopify

- Become shopify partner, it help you create developement stores for free for unlimited.
- In developer store, you can have maximum 50 real orders and unlimited test/fake orders.

## Shopify Theme

- [Shopify CLI instllation commands Guide](https://shopify.dev/docs/themes/tools/cli/install)

- [Shopify CLI theme commands](https://shopify.dev/docs/themes/tools/cli/commands)

- [Shopify theme architecture](https://shopify.dev/docs/themes/architecture)

- [Liquid Reference](https://shopify.dev/docs/api/liquid)

- [Shopify Cheat Sheet](https://www.shopify.com/partners/shopify-cheat-sheet)

### [What's new in Shopify Store 2.0](https://www.shopify.com/partners/blog/shopify-online-store)

- **Online Store Design:* The new version offers more than 100 customizable templates to choose from, along with drag-and-drop editing tools to make changes to your website design easily.

- **Improved Performance:** Shopify Store 2.0 boasts faster page loading times and improved site performance.

- **Enhanced Navigation:** Navigation menus and page layouts can now be customized, allowing merchants to create a more personalized shopping experience for their customers.

- **Sections and Blocks:** Shopify Store 2.0 includes a new Sections and Blocks system that allows merchants to easily add and rearrange content on their online store.

- **Advanced Product Filtering:** The platform has an improved product filtering system that makes it easier for customers to find products on the store.

- **Multilingual Support:** The new version offers multilingual support, allowing merchants to create a store that caters to customers from different countries and languages.

## [Shopify Theme Architecture](https://shopify.dev/docs/themes/architecture)

Shopify theme files fall into following 3 categories

### Markup and features

- These files control the layout and functionality of a theme. 

- They use Liquid to generate the HTML.


### Supporting assets

- These files are **consumed** by other files in the theme. They include

**-** assets

**-** scripts

**-** locale files

### Config files

- These files can be **customized** by merchants using the theme editor. They include

**-** JSON to store configuration data

## Shopify Theme Directory Structure 

![20210709003729_directory](https://user-images.githubusercontent.com/204423/224762348-491596ff-2006-446f-adac-1942b02dfc34.jpg)


## Shopify Theme Flow

![20210702001604_overallstructure-100](https://user-images.githubusercontent.com/204423/224762907-4e659333-6155-418f-9888-a9dd39506a79.jpg)

### Layout

- All themes starts from **Layout** files.

- You put them in **layout** folder.

- All themes **MUST** have a default layout file, named `theme.liquid` - the default theme layout for all non-checkout pages => It provide header, content placeholder (template files). It act like container for all of your **pages** for the themes e.g; 404, index, collections, checkout etc.

```
<!DOCTYPE html>
<html>
  <head>
   {{ content_for_header }}
  </head>

  <body>
    {{ content_for_layout }}
  </body>
 </html>

```

- `checkout.liquid` - This layout file is used on checkout page. 


![20210629175318_Screen Shot 2021-06-29 at 10 51 01 AM](https://user-images.githubusercontent.com/204423/224764848-3d19220f-3834-48d0-bc46-d5c6033f3c8a.jpg)

## Templates (Pages)

- Each page in shopify theme have a associated template.
- By default, this template will be hosted by `theme.liquid` layout.
- But you can tell in the template file, if you wanted to change that.

- https://www.shopify.com/partners/blog/84342470-the-power-of-alternate-layout-files-in-shopify-theme-development
- https://www.shopify.com/partners/blog/shopify-alternate-templates
- https://shopify.dev/docs/themes/architecture/templates/json-templates#schema


## Sections

- Section files are used to host **reusable modules** of content that can be **customized by merchants**. 

- Sections have the same access to **global objects, tags, and filters** as other Liquid theme files, as well as **2 section-specific objects:** the section object and the block object.

### Day to Day 

#### Starting a Theme Project

`shopify theme init -u url_to_base_theme`


#### Running the Theme

`shopify theme dev -s url_to_your_store`

If you are starting from scratch, you can check my min theme @ https://github.com/itsaboutcode/shopify_min_theme

### Shopify Theme Pages

Shopify have set of possible pages, which you can build and they can be accessed from a certain url.

- 404
- article
- blog
- cart
- collection
- customers/account
- customers/activate_account
- customers/addresses
- customers/login
- customers/order
- customers/register
- customers/reset_password
- gift_card.liquid
- index
- list-collections (/collections)
- page
- password
- product
- robots.txt.liquid
- search


## Shopify Developer



# Reference

- https://www.shopify.com/partners
- https://partners.shopify.com/
- https://shopify.dev/docs
- https://help.shopify.com/en
- https://apps.shopify.com/
- https://shopify.dev/docs/api/liquid
- https://partner-training.shopify.com/
