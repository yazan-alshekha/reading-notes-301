## DELEGATING EVENTS

In this example, the event
handler will run when users click
or mouseover items in the list,
except for the last list item. 

It writes out the content of the
element the user interacted with,
a status message (using the data
property), and the event type. 

The information passed in the
data property here uses object
literal notation (so it could
handle multiple properties). 

1.  The event handler is triggered
by cl ick and mouseover events. 

2. The selector parameter
filters out the element whose id
attribute has a value of four. 

3.  Additional data that will be
used by the event handler is
passed in as an object literal. 


4. The event handler uses the
event object to display the
content of the element the user
interacts with, the information
from the data that was passed
into the function, and the event
type, under the list in a white box


## the best place to hold script JQuery

Befor The closing `<body>` Tag

this is an ideal location as
1. The script is not blocking other things from downloading

2. The DOM has already loaded by the time the script is executed
