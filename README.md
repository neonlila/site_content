# Tutorial - Site Content
Create your own custom content blocks

## Folder structur
- Configuration
    - Sets
        - SiteContent
            - config.yaml
            - page.typoscript
            - settings.yaml
- ContentBlocks
    - ContentElements
        - badge-element
        - button-element
        - list-group
        - simple-card
- Resources
    - Public
        - ContentBlocks

## Installation & Setup
composer req tutorial/site-content
- This site-content package is dependent on EXT:content_blocks

1. Go to Sites -> setup
2. Click on "Edit site configuration"
3. Scroll down to "Sets for this Site"
4. Choose "Tutorial SiteContent" in Available Items
5. Save

## Create new blocks
```
ddev typo3 content-blocks:create

or

./vendor/bin/typo3 content-blocks:create

### Follow the steps
- Choose the content type -> content-element
- Define vendor name. If you are working within this extention (vendor name = tutorial)
- Define content-block-name
- Define the title of your new block
- Choose the extension your content block should be stored in

### After creating your block
```
ddev typo3 extension:setup --extension=site_content

or 

./vendor/bin/typo3 extension:setup --extension=site_content

and 

ddev typo3 cache:flush

or 

./vendor/bin/typo3 cache:flush

## TODOs
[x] create some basic elements
[ ] create some advanced elements like - slider, accordeon etc.
[ ] add locallang.xlf for german language
[ ] columns elements