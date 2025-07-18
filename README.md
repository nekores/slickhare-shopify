# Slickhare Shopify Theme

## Prerequisites
- [Shopify CLI](https://shopify.dev/docs/themes/tools/cli) installed
- Access to a Shopify store (store URL)
- Node.js and npm (for some advanced theme development workflows)

## Getting Started

### 1. Install Shopify CLI
On macOS (using Homebrew):
```sh
brew tap shopify/shopify
brew install shopify-cli
```
Or see [Shopify CLI installation docs](https://shopify.dev/docs/themes/tools/cli/installation) for other platforms.

### 2. Log in to Your Shopify Store
```sh
shopify login --store your-store-name.myshopify.com
```
Replace `your-store-name` with your actual store name.

### 3. Run the Theme Locally (Development Server)
From the theme directory, run:
```sh
shopify theme dev
```
- This will upload your theme as a development theme and provide a preview URL.
- Live reload is enabled for theme file changes.
- If you get a port error, use a different port:
  ```sh
  shopify theme dev --port=9293
  ```

### 4. Push Theme to Shopify Store
To upload your local theme to your Shopify store:
```sh
shopify theme push
```
- This will create a new unpublished theme in your store.
- To update a specific theme, first list your themes:
  ```sh
  shopify theme list
  ```
  Then push to a specific theme by ID:
  ```sh
  shopify theme push --theme <theme-id>
  ```

### 5. Publish or Preview Your Theme
- Go to **Online Store > Themes** in your Shopify admin.
- Preview or publish the uploaded theme as needed.

## Adding Judge.me Reviews Widget
- The theme includes a dynamic section for Judge.me reviews.
- In the Shopify customizer (**Online Store > Themes > Customize**), click **Add section** and select **Judge.me Reviews** to add the reviews widget to any page.

## Troubleshooting
- **Port in use:** Use `--port` flag with a different port number.
- **Asset overwrite error:** Remove duplicate or conflicting files in the `assets/` folder.
- **Judge.me widget not showing:** Ensure you have reviews marked as "featured" in Judge.me, and that the app is installed and configured.

## Resources
- [Shopify Theme Development Docs](https://shopify.dev/docs/themes)
- [Shopify CLI Reference](https://shopify.dev/docs/api/cli)
- [Judge.me Help Center](https://help.judge.me/) 