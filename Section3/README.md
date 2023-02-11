# HTML Refresher
HTML, which stands for Hypertext Markup Language, is the standard markup language used for creating web pages. An HTML document is made up of a series of HTML elements, which are used to define the content and structure of the page.

The basic structure of an HTML document consists of several parts:

The <!DOCTYPE> declaration, which specifies the version of HTML being used.

The ```<html>``` element, which contains all of the other elements on the page.

The `<head>` element, which contains information about the page that is not displayed to the user, such as the page title, meta tags, and links to stylesheets.

The `<body>` element, which contains all of the visible content on the page, such as text, images, and links.


### Basic HTML Structure
```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>Heading 1</h1>
    <p>This is a paragraph.</p>
  </body>
</html>

```
In this example, the `<!DOCTYPE>` declaration specifies that the document is using HTML5. The `<html>` element contains the `<head>` and `<body>` elements, and the `<head>` element contains a `<title>` element with the page title. The `<body>` element contains an `<h1>` element with the text "Heading 1" and a `<p>` element with the text "This is a paragraph."


### HTML Tags
HTML tags are the building blocks of an HTML document. They are used to define the structure and content of a web page. An HTML tag is surrounded by angle brackets (< and >), and usually comes in pairs - an opening tag and a closing tag - with the content to be enclosed in between.

For example, the `<p>` tag is used to define a paragraph of text, and the opening tag is `<p>` and the closing tag is `</p>`. Any text that comes between these two tags will be rendered as a paragraph on the web page.

HTML tags can also have attributes, which provide additional information about the tag. For example, the `<img>` tag is used to insert an image on the page, and it has attributes such as src to specify the URL of the image, alt to provide a description of the image, and width and height to specify the dimensions of the image.

Here are a few examples of common HTML tags:

- `<h1>` to `<h6>`: heading tags to define headings and subheadings.

- `<p>`: paragraph tag to define a paragraph of text.

- `<a>`: anchor tag to define a hyperlink to another web page or resource.

- `<img>`: image tag to insert an image on the page.

- `<ul>` and `<li>`: unordered list and list item tags to create bulleted lists.

- `<ol>` and `<li>`: ordered list and list item tags to create numbered lists.

- `<div>`: division tag to group together other HTML elements and apply styles to them.

- `<span>`: inline tag to apply styles to a small section of text.

There are many other HTML tags available that can be used to define a variety of content on a web page, such as tables, forms, and media players. By combining these tags in different ways, web developers can create complex and dynamic web pages with a rich user experience.


### HTML attributes

HTML attributes are additional pieces of information that can be added to an HTML tag. They provide extra information about the tag, and can be used to control the behavior or appearance of the element.

Attributes are added to an HTML tag using the attribute name and value in the opening tag. The syntax for an attribute is:

```
<tagname attribute="value">
```

For example, the <a> tag, which is used to create links to other pages or resources, has several attributes that can be used to control the behavior of the link, such as the href attribute to specify the destination URL, the target attribute to control where the link opens, and the title attribute to provide a tooltip for the link.

Here are a few examples of common HTML attributes:

- **class**: Used to specify one or more classes for an HTML element, which can be used to apply CSS styles.

- **id**: Used to give an HTML element a unique identifier, which can be used to target the element with JavaScript or CSS.

- **src**: Used to specify the source URL for an image or other media element.

- **href**: Used to specify the destination URL for a link.

- **title**: Used to provide additional information about an HTML element, such as a tooltip or description.

- **alt**: Used to provide alternative text for an image or other media element, which is displayed when the element cannot be rendered.

In addition to these common attributes, there are many others that can be used to control the behavior and appearance of HTML elements. By using attributes in combination with HTML tags and CSS styles, web developers can create complex and dynamic web pages with a rich user experience.


### HTML Elements

HTML elements are the basic building blocks of an HTML document. They define the structure and content of a web page and provide meaning to the various parts of the page. An HTML element consists of a starting tag, the content, and an ending tag. It may or may not have attributes.

The starting tag begins with the less-than symbol (<), followed by the name of the element, and ends with a greater-than symbol (>). The ending tag is similar to the starting tag, but it includes a forward slash (/) before the element name.

For example, the HTML element for a paragraph of text is defined using the <p> tag. The starting tag is <p> and the ending tag is </p>. Any text or other content that is enclosed between these tags is considered part of the paragraph.

HTML elements can also include attributes that provide additional information about the element, such as the href attribute for a hyperlink or the src attribute for an image. These attributes are included in the opening tag of the element and are used to provide further information about the element.

Some common HTML elements include:

`<html>`: the root element of an HTML document.

`<head>`: the container for metadata and other information about the web page.

`<body>`: the container for the content of the web page that is displayed in the browser.

`<p>`: defines a paragraph of text.

`<a>`: defines a hyperlink to another page or resource.

`<img>`: defines an image that is displayed on the page.

`<ul>` and `<li>`: defines an unordered list and its list items.

`<ol>` and `<li>`: defines an ordered list and its list items.

`<div>` and `<span>`: generic container elements used to group and apply styles to other elements.

By combining these and other HTML elements in various ways, web developers can create rich, dynamic web pages that are both functional and visually appealing.