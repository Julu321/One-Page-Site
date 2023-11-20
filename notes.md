HAMBURGER MENU:



1. menu-btn-container:
Is a label used as a container for the icon. 
A label is used to "store" or "assign" elements to a bigger place. 
In this exaple if we click that place we will trigger the button.

Adventages:
The label text is not only visually associated with its corresponding text input; 
it is programmatically associated with it too. This means that, for example, a screen reader
will read out the label when the user is focused  the form input, making it easier for an assistive
technology user to understand what data should be entered.


When a user clicks or touches/taps a label, the browser passes the focus to its associated input. 
That increased hit area for focusing the input provides an advantage to anyone trying to activate it
 — including those using a touch-screen device.

Here’s how it’s used in the code:

display: none;: This property initially hides the .menu-button-container. It’s not visible on the page when the page first loads or on larger screens.

height: 100%; width: 30px;: These properties set the height and width of the .menu-button-container.

cursor: pointer;: This property changes the cursor to a pointer when hovering over the .menu-button-container, indicating an interactive element.

flex-direction: column; justify-content: center; align-items: center;: These properties use Flexbox to center the hamburger menu icon vertically and horizontally within the .menu-button-container.

In the media query @media (max-width: 700px), the display property is changed to flex, which makes the .menu-button-container visible on screens smaller than 700px wide. This is typically when the navigation menu switches to a collapsed, hamburger-style menu for mobile or smaller screens.

2. menu-toggle:
Is a checkbox that controls whether the mobile navigation menu is open or closed.

3. menu-btn
The piece of code with .menu-btn,.menu-btn::before,.menu-btn::after creates three white lines 
................
.menu-btn,
.menu-btn::before,
.menu-btn::after {
  display: block;
  background-color: #fff;
  position: absolute;
  height: 4px;
  width: 30px;
  transition: transform 400ms cubic-bezier(0.23, 1, 0.32, 1); 
  border-radius: 2px;
}


.menu-btn::before {
    content: '';
    margin-top: -8px
  }
  
.menu-btn::after {
    content: '';
    margin-top: 8px;
  }

................

display block - causes a line break before and after the element. In the context of this code, it means that the .menu-btn, .menu-btn::before, and .menu-btn::after will each appear on their own line within the .menu-button-container.

postion absolute - the elements are taken out of the normal flow of the documet

transition - ads animation and it's duration.

The content: ''; property is necessary for the pseudo-element to be generated.

The margin-top: -8px; property moves the pseudo-element up by 8 pixels from its original position, creating the top line of the hamburger icon.


