# h1 Heading
## h2 Heading
### h3 Heading

Headings 4, 5, and 6 are not styled so do not use!

## Horizontal Rules
These will create a line break. It is made of 3 underscores!
___


## Emphasis
You can use either of these methods to make bold or italic text. It does not matter!

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

## Blockquotes


> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.


## Lists

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


## Code

Inline `code`

Code Blocks
```
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```

## Tables
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


## Links

[Regular Link](https://www.rustyoperations.net/img/rust-logo.jpg)

[Titled Link (Hover Over Me)](http://www.rustyoperations.net "Rusty Operations Community Website")


## Images

![Alt text][id]

Below can be placed anywhere in the text, as long as what you put in the second pair of square brackets is the same! The text at the end of the below line in quotes is what users can see if they hover over the picture with their mouse. This is not required. Alt text is what a screenreader will use.

[id]: https://www.rustyoperations.net/img/rust-banner.jpg  "Rusty Operations Banner"


## Abbreviations

This is <abbr title="Hyper Text Markup Language">HTML</abbr> abbreviation example.

## Timestamps

Each article needs a timestamp in its metadata to show when it was last updated. These timestamps can be generated [here](https://timestampgenerator.com/). You will need to get the `ICO 8610` format, otherwise it will not work. For example, UK Time 22/07/2023 16:00:00 BST will be 2023-07-22T15:00:00+0000 in universal time. The website wil generate the timestamp for the current time for you.