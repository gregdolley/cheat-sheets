# Markdown Cheat Sheet

This is a WIP and not complete yet...

## The Basics

<table>
    <th>Element</th><th>MD Syntax</th>
    <tr>
        <td>Heading 1</td><td>#</td>
    </tr>
    <tr>
        <td>Heading 2</td><td>##</td>
    </tr>
    <tr>
        <td>Heading 3</td><td>###</td>
    </tr>
    <tr>
        <td>Bold text</td><td>**<b>Bold text</b>**</td>
    </tr>
    <tr>
        <td>Italic text</td><td>*<I>Italic text</I>*</td>
    </tr>
    <tr>
        <td valign="top">Ordered List</td><td><ol><li>First item</li><li>Second item</li><li>Third item</li></ol></td>
    </tr>
    <tr>
        <td valign="top">Unordered List</td><td><ul><li>First item</li><li>Second item</li><li>Third item</li></ul>(Replace the bullet char above with either: "-", "*", or a "+" symbol. Like this:<br/><br/>
        + Item 1<br/>
        + Item 2<br/>
        + Item 3<br/>
        </td>
    </tr>
    <tr>
        <td>Horizontal divider</td><td>---</td>
    </tr>
    <tr>
        <td>Text link</td><td>[display text for link](https://www.URL-target-for-link.com)</td>
    </tr>
    <tr>
        <td>Image</td><td>![ALT text](path_to_image.jpg "Optional title attribute")</td>
    </tr>
    <tr>
        <td>Inline code</td><td>`code here`</td>
    </tr>
    <tr>
        <td>Block Quotes</td><td> &gt;&nbsp;Example using<br/>&gt;&nbsp;block quoted text</td>
    </tr>
</table>

## Extended Syntax

These elements are not supported by all Markdown applications.

<table>
    <th>Element</th><th>MD Syntax</th>
    <tr>
        <td valign="top">Fenced code block or terminal output <br/><br/>(With language specific coloring)</td><td>```javascript<br/>let input = get_user_input();<br/>console.log("Received:", input);<br/>```
        <br/><br/>```bash<br/>User@domain:~$ la -al --color<br/>```</td>
    </tr>
    <tr>
        <td valign="top">Table</td><td>| Column 1 | Column 2 |<br/>
|----|----|<br/>
| Col 1 text | Col 2 text |<br/>
| Second row text | More text |</td><br/>
    </tr>
    <tr>
        <td valign="top">Footnote</td><td>Sentence with a footnote. [^1]<br/><br/>[^1]: This is the footnote.</td>
    </tr>
    <tr>
        <td>Strikethrough</td><td>~~Text that needs strikethrough~~</td>
    </tr>
    <tr>
        <td valign="top">Task list</td><td>- [x] Write code.<br/>- [ ] Run unit tests.<br/>- [ ] Write documentation.</td>
    </tr>
    <tr>
        <td valign="top">Latex math block</td><td>$$<br/>f\left(a\right) = \sum_{n=a}^{\infty} n<br/>$$</td>
    </tr>
</table>

The Latex math block example above would result in the following math text (assuming your Markdown reader supports it):

$$
f\left(a\right) = \sum_{n=a}^{\infty} n
$$
