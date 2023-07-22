# h1 Heading
## h2 Heading
### h3 Heading

Headings 4, 5, and 6 are not styled so do not use!

## Formatting

### Horizontal Rules
These will create a line break. It is made of 3 underscores!
___


### Emphasis
You can use either of these methods to make bold or italic text. It does not matter!

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

### Blockquotes


> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.


### Lists

Unordered

+ Create a list by starting a line with `+`, `-`, or `*`
+ Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    * Ac tristique libero volutpat at
    + Facilisis in pretium nisl aliquet
    - Nulla volutpat aliquam velit
+ Very easy!

Ordered

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa

Start numbering with offset:

57. foo
1. bar


### Code

Inline `code`

Code Blocks
```
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```

### Tables
For tables, it is important you wrap them in a div object with the classes, as follows. If you do not to this, the table will not be scrollable on smaller devices and break the webpage!
<div class="table-width scroll-bar">
  <table class="table">
  <tr>
    <th>Name</th>
    <th>IP</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>3x</td>
    <td>64.40.9.19:28024</td>
    <td>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi imperdiet placerat quam in pulvinar. Morbi elementum molestie nisl a eleifend. Vestibulum auctor turpis non facilisis interdum. Maecenas facilisis mattis nulla, eu porttitor dolor accumsan et. Donec sed consequat quam. Quisque lectus velit, tempor non erat ut, tincidunt vehicula quam. Quisque volutpat eget odio quis volutpat. Ut placerat, erat ut viverra varius, leo justo suscipit elit, ut pulvinar mi diam id ipsum. Nunc vehicula mattis eleifend. Vivamus a gravida dui. Vivamus malesuada libero a finibus gravida.</td>
  </tr>
  <tr>
    <td>2x</td>
    <td>0.0.0.0</td>
    <td>Lorem ipsum dolor sit amet, consectetur adipiscing elit. In sodales quam non tristique sollicitudin. Integer id est vulputate, pretium erat non, pellentesque enim. Quisque scelerisque vel sapien vitae bibendum. Sed rutrum molestie nunc, nec viverra mi pretium in. Aenean quis mi finibus, fringilla lacus in, feugiat lorem. Duis porta tellus quis turpis sollicitudin, et ultricies dui volutpat. Ut quis ante lacus. Praesent pellentesque mauris in justo dignissim efficitur. Morbi faucibus laoreet urna, et aliquam purus accumsan non. Morbi pellentesque placerat urna eu pretium. Sed eu aliquet lacus, ac aliquet est. Pellentesque vestibulum dolor et nunc fringilla, at cursus nunc convallis. Suspendisse sed risus ut dolor vulputate posuere non sed dui. Aenean fermentum gravida orci at vulputate.</td>
  </tr>
  </table>
</div>


### Links

[Regular Link](https://www.rustyoperations.net/img/rust-logo.jpg)

[Titled Link (Hover Over Me)](http://www.rustyoperations.net "Rusty Operations Community Website")


### Images

<div class="grid grid-cols-2">
  <img src="https://www.rustyoperations.net/img/rust-banner.jpg" alt="alt text">
  <img src="https://www.rustyoperations.net/img/rust-banner.jpg">
</div>


### Abbreviations

This is <abbr title="Hyper Text Markup Language">HTML</abbr> abbreviation example.


## Writing Your Own Article

This section will teach you how to write your own article and publish it to the website!

### Getting Started

You can write your own markdown files! It's super easy! I would recommend using [VSCode](https://vscode.dev/) which you can access in your browser. This is because it lets you preview the Markdown file!

Once you are on https://vscode.dev/github, click Open Remote Repository and select `OperationsCentre/articles`

Congradulations! You have now successfully logged into VSCode and you can start making your articles!

You can also download the desktop application, but it's not required!

### Writing your first article
Depending on what you're writing, you will create a new .md file in the news or forums folder. Feel free to create subfolders too, to keep things organised. It does not matter what you call them, so name it something memorable and descriptive!

You can already see a lot of articles have been made!

Follow the above guide on how to style an article!

REMEMBER: Any images you upload, will not be accessible until you commit the changes, but you can still add the images in the .md file like above! The images folder is https://articles.rustyoperations.net/images/`imagefile`.

### Uploading your article to GitHub
Once you have finished editing your article, it's time to upload it publicly!

To do so, make sure all your files are saved, then go to the Soruce Control tab on the side. Add a commit message and press the `Commit & Push` button. Well done! Your article is ready to be put on the website! 

### Publishing your article
Follow the instruction on the [Admin Panel](https://admins.rustyoperations.net/)

### How to get the URL of my article
Once your article is pushed to GitHub, you can get the file by doing to it's directory. The director follows the stucture of https://articles.rustyoperations.net/`article-name.md` where `articleName` is the director it's stored. For example, this tutorial is stored here: https://articles.rustyoperations.net/tutorial.md. There are other articles too. For example, the forums are https://articles.rustyoperations.net/forums/`forum-name`.

### How to link articles together
The website has an override parameter in the forums and news view page. To link to an article, you simply create a hyperlink like so: [Linked Article](https://rusty-operations-community-website-test.web.app/forums/view?override=https://articles.rustyoperations.net/tutorial.md). Even though users cannot access this from the forums page, the override will render any Markdown file you pass in. The Markdown file doesn't even have to me one of ours. As long as it's a Markdown file, it will render!

### Timestamps
Each article needs a timestamp in its metadata to show when it was last updated. These timestamps can be generated [here](https://timestampgenerator.com/). You will need to get the `ICO 8610` format, otherwise it will not work. For example, UK Time 22/07/2023 16:00:00 BST will be 2023-07-22T15:00:00+0000 in universal time. The website wil generate the timestamp for the current time for you.
