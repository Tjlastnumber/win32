---
Description: The Text control displays static text, which may use a predefined style.
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: Text Control
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Text Control

The Text control displays static text, which may use a predefined style.

The recommended method for displaying text with specified line breaks is to use multiple one-line text controls located below each other. The character sequences \\n, \\r\\n, or \\n\\r in the text field for the control are not displayed as a line break. These character sequences are literally displayed by the control.

## Control Attributes

You can use the following attributes with the Text control. To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column. Enter the identifier of the ControlEvent in the Event column.



| Attribute identifier                                             | Hexadecimal bit                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)                       |                                  | Position of control in the dialog box. Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md). Use [installer units](installer-units.md) for length and distance.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Text](text-control-attribute.md)                               |                                  | Text displayed by the control. To set the font and font style of a text string, prefix the string of displayed characters with {\\style} or {&style}. Where style is an identifier listed in the TextStyle column of the [TextStyle table](textstyle-table.md). If neither of these are present, but the [**DefaultUIFont**](defaultuifont.md) property is defined as a valid text style, that font will be used.<br/>                                                                                                                                                                                                                                                                                                                              |
| [TimeRemaining](timeremaining-control-attribute.md)             |                                  | This attribute enables a Text control to display the approximate number of minutes and seconds remaining for an installation. Subscribe the Text control to the [TimeRemaining ControlEvent](timeremaining-controlevent.md) in the [Eventmapping table](eventmapping-table.md) and enter TimeRemaining into the Attribute column.<br/> The installer publishes a record containing one integer representing the number of seconds remaining in the installation. Include a row in the [UIText table](uitext-table.md) with TimeRemaining in the Key column. Enter a formatted text string into the Text column authored to display minutes and seconds. Format this string as described for [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).<br/> |
| [Visible](visible-control-attribute.md)                         | 0x00000000 0x00000001<br/> | Hidden control. Visible control.<br/> Include this bit in the bit word of the Attributes column in the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md).to make the control visible or hidden upon its creation.<br/> You can also hide or show a control by using the [ControlCondition table](controlcondition-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [Enabled](enabled-control-attribute.md)                         | 0x00000000 0x00000002<br/> | Control in a disabled state. Control in an enabled state.<br/> Include this bit in the bit word in the Attributes column of the [Control](control-table.md) or [BBControl tables](bbcontrol-table.md) to enable the control on creation.<br/> You can also enable or disable a control by using the [ControlCondition table](controlcondition-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| [Sunken](sunken-control-attribute.md)                           | 0x00000000 0x00000004<br/> | Displays the default visual style. Displays the control with a sunken, 3-D, look.<br/> Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [RTLRO](rtlro-control-attribute.md)                             | 0x00000000 0x00000020<br/> | Text in the control is displayed in left-to-right reading order. Text in the control is displayed in right-to-left reading order.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [RightAligned](rightaligned-control-attribute.md)               | 0x00000000 0x00000040<br/> | Text in the control is aligned to the left. Text in the control is aligned to the right.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Transparent](transparent-control-attribute.md)                 | 0x00000000 0x00010000<br/> | Opaque control. Background shows through control. The control has the WS\_EX\_TRANSPARENT style.<br/> Include this bit in the Attributes column of the [Control](control-table.md) or [BBControl tables](bbcontrol-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [NoPrefix](noprefix-control-attribute.md)                       | 0x00000000 0x00020000<br/> | Use & in a text string to display the next character as underscored. The character & in a string is displayed as itself.<br/> Include this bit in the bit word in the Attributes column of the [Control](control-table.md) or [BBControl tables](bbcontrol-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [NoWrap](nowrap-control-attribute.md)                           | 0x00000000 0x00040000<br/> | Text wraps. Text is displayed on a single line. If the text extends beyond the control's margins, it is clipped and an ellipsis ("...") is inserted.<br/> Include this bit in the bit word in the Attributes column of the [Control](control-table.md) or [BBControl tables](bbcontrol-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [UsersLanguage](userslanguage-control-attribute.md)             | 0x00000000 0x00100000<br/> | Fonts created in the database code page. Fonts created in the user's default UI code page.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [FormatSize Control Attribute](formatsize-control-attribute.md) | 0x00000000 0x00080000<br/> | Formatted as text. If this bit is set the control attempts to format the displayed text as a number representing a count of bytes. For proper formatting, the control's text must be set to a string representing a number expressed in units of 512 bytes. The displayed value will then be formatted in terms of kilobytes (KB), megabytes (MB), or gigabytes (GB), and displayed with the appropriate string representing the units.<br/>                                                                                                                                                                                                                                                                                                          |



 

## Remarks

This control can be created from the STATIC class by using the [**CreateWindowEx**](https://www.bing.com/search?q=**CreateWindowEx**) function. It has the **SS\_LEFT**, **WS\_CHILD**, and **WS\_GROUP** styles.

Do not place transparent Text controls on top of colored bitmaps. The text may not be visible if the user changes the display color scheme. For example, text may become invisible if the user sets the high contrast parameter for accessibility reasons.

 

 



