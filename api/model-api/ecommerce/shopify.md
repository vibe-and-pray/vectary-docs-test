# Shopify

## Introduction

Shopify is one of the big players in the e-commerce scene. If you are ready to create an amazing showcase for your products and as well as create a great shopping experience for your clients, use this step by step guide to learn how to add an interactive and customizable 3D models from Verctary.

For this guide we will use a `free` template that Shopify provides when creating a new shop called `Dawn`.

This integration **does require minor changes to the templates**, but do not worry, the process is fast and easy.

<figure><img src="../../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>



## Requirements



For integrating with `Shopify` you will need the following:

* A Shopify account with an active `free trial` or `paid subscription`





## Vectary setup



### 1.1. Create a folder for the product models

This is an important part of any integration. **Use the id of the folder to fetch and map your models to the products** you have/will setup in the e-shop.

You can see the id when it is selected inside the [Dashboard](https://vectary.com/dashboard), directly in the URL after the string `&folderId=`.

### 1.2. Create the model of your product/s

In this case, we created an abstract design called `Awesomeness`. **The name of your project needs to match the name of your product**.

Here is the model you can clone directly into a new project in your workspace: [https://www.vectary.com/p/5s8oStuOPjH9E2xrRVje3q](https://www.vectary.com/p/5s8oStuOPjH9E2xrRVje3q)\
\
It features a `Variant` with 3 different objects, and each of the variants contains the same 3 materials. **Make sure to link the materials if they are the same between each variant**.

We can expose these through the `Floating UI` by adding a `Materials` and a `Variants` sub-objects.

Please note that the `source` of the MSController is the Object Switcher containing the variants.

&#x20;![](<../../../.gitbook/assets/image (123).png>)         ![](<../../../.gitbook/assets/image (124).png>)



### 1.3. Share your model

Go ahead and [share](../../../documentation/sharing-exporting-embedding/sharing.md)

Please remember that:

* The name of the project matches the name of the product.
* The names of the objects and their materials match the options/variants that are setup for the product in the e-shop.





## Shopify’s setup



### 2.1. Add products

First of all we need to make sure we have at least one product. Remember that **the names of the products need to match the names of the models** we are creating in Vectary.

For the purposes of covering all the options that are possible in this guide, we are going to use a product with `options` (that will generate `variants`).

To add options to a product simply edit the chosen product, scroll down to the `Options` section and start adding.

<figure><img src="../../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>

If the default Option names do not match with what you would need, please look for a plugin/app instead of using the defaults from Shopify.

<figure><img src="../../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

In this case, here are the options that we’ll be working with, and that mimic what we have setup in Vectary.

From these options the `variants` are then generated. It is possible to manage price and inventory individually for each one.

<figure><img src="../../../.gitbook/assets/image (138).png" alt="" width="302"><figcaption></figcaption></figure>



### 2.2. Add the iframe and api script



Now, edit the theme. To do that, we will select the Themes page under our Online Store.

<figure><img src="../../../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

In our case we are working with Shopify’s default Dawn theme (v12.0.0).

<figure><img src="../../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

What we want to do is to click on the Edit code button.

<figure><img src="../../../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

A new view will open. Search for a specific file called product-media-gallery.liquid, which should be under the Snippets folder.

<figure><img src="../../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

Look for the container that holds the [`Media`](https://help.shopify.com/en/manual/products/product-media). Add it to the products, and then add our custom code.

Here’s how to find it:

* Click anywhere in the code
* Press `ctrl+f`(Windows) or `cmd+f`(Mac)
* Paste the text `id="Slider-Gallery-{{ section.id }}`
* Hit intro

You should be able to see (or similar) as selected:

<figure><img src="../../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

If you don’t find it, that probably means your theme is set differently.

{% hint style="danger" %}
In older theme versions this code we located in the main-product.liquid file, under the Sections folder. Check it out in case you don’t find it there.
{% endhint %}

Please [get in touch with us](https://www.vectary.com/contact-us/) or contact your sales representative, and we will assist you in figuring out a solution.

Paste the following code under the last line in the previous screenshot:

```javascript
<!-- My Vectary integration start -->
<li class="product__media-item grid__item slider__slide is-active">
  <iframe id="vectary_embed" 
		src="https://app.vectary.com/p/{shared_model_id}" 
		frameborder="0" 
		width="100%" 
		height="480">
	</iframe>
</li>
<script type="module">
  // Init Model API
	import { VctrModelApi } from "https://app.vectary.com/studio-lite/scripts/api.js";
  var modelApi = new VctrModelApi("vectary_embed");
  await modelApi.setShopify("{folder_id}", "{{ product.title | escape }}");
</script>
<!-- My Vectary integration end -->
```



Let’s analyze exactly what we are adding to make sure everything is how it is supposed to be:

1. `li` element that contains the iframe of our embed.
   1. We added the same `class` names that are used for any other media that is used in our current theme.
2. `iframe` element that contains **any of your shared projects in the folder** we created.
   1. You need to change the `{shared_model_id}` in the `src` attribute for a valid id.

{% hint style="info" %}
Do not worry about which of the product ids you add here. The script will take care of selecting the right product id from your folder based on the `product.title`, but Shopify needs to have a valid `src` input, otherwise it will not allow to load the `iframe`.&#x20;
{% endhint %}

&#x20;        b. Replace the iframe code directly from the Copy embed button in Vectary share popup - [sharing.md](../../../documentation/sharing-exporting-embedding/sharing.md "mention")



3. `script` tag which in turn:
   1. Imports our `VctrModelApi`.
   2. Creates a new instance of the API, linking to the `iframe` embed we just added using its DOM `id` (e.g. `vectary_emebed`).
   3. Sets the integration with `{folder_id}` from step **#1.1**



Don’t forget to Save!



One more thing to consider, in case you just want to use the Vectary embed to showcase your product and/or **you will not add any other pictures**. Please note that some themes can change the layout of the product page when they detect that there is no media attached.

To avoid that do the following:

* Search for & open the `main-product.liquid` file
* Press `ctrl+f`(Windows) or `cmd+f`(Mac)
* Paste `if product.media.size > 0` in the `Find` field
* Paste `if product.media.size >= 0` in the `Replace` field\
  ![](<../../../.gitbook/assets/image (144).png>)
* Click on the `replace all` button and `Save`



If your product names match the model names, and if the product options also match the names of the materials and objects used, you should be able to see how they influence each other in the product page:

<figure><img src="../../../.gitbook/assets/test.gif" alt=""><figcaption></figcaption></figure>

It also works by default with a different `Variant picker` type.

You can select another type when you `Customize` your theme in the `Default product` page.\
\
![](<../../../.gitbook/assets/image (145).png>)

![](<../../../.gitbook/assets/image (148).png>)

![](<../../../.gitbook/assets/image (149).png>)<br>
