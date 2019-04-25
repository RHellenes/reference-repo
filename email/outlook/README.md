# Protips

###### Based on articles listed below 

- [How to Code Emails for Outlook 2016](https://www.emailonacid.com/blog/article/email-development/how-to-code-emails-for-outlook-2016/)
- [Creating Bulletproof HTML Emails - Pro Tips & Tricks to Make Your Life Easier](https://medium.com/tealmedia/creating-bulletproof-html-emails-e0e4866c3f8)


## Legend

1. [Outlook conditional tags](#outlook-conditional-tags)
2. [Margins](#margins)



## Outlook conditional tags
- [Documentation](https://docs.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537512(v=vs.85))

Syntax: `<!--[if expression]> HTML <![endif]-->`

Eks:

```html
Target Outlook 2000, 2002, & 2003:
  <!--[if mso]>
    <style type="text/css">
      /* Your styles here */
    </styles>
  <![endif]-->

Target Outlook 2000, 2002, & 2003
<!--[if IE]>
  <style>
     /*Your styles here*/
  </style>
<![endif]-->

Target all Outlook versions
<!-- [if (gte mso 9) | (IE)]>
  <style>
      /*Your styles here*/
  </style>
<![endif]-->
```

## Margins and paddings on images

Outlook ignores inline or embedded styles that add padding or margins to images. To get around this, wrap the image in a table with margin, padding, or cellpadding depending on how much space you need.

```html
  <table style="padding:30px">
    <tr>
      <td  style="background:#ff0000; padding:10px;">
        <img src="#" alt="#">
      </td>
    </tr>
  </table>
```