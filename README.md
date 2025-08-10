Vibe coding with Firebase Studio to create a food ordering app.

Inspiration: A friend operating her home restaurant business is having trouble 
streamlining customer orders and relies on personal messaging via WhatsApp to send menu 
and receive orders. 

Prompt for Firebase Studio, refined with ChatGPT:

----------------------------------------------
```Build a food ordering app with the following requirements:

Use Firebase for hosting, Firestore for data storage, and Firebase Auth (optional) for admin login.

The app has two user roles:
Customer (no login, just interacts with menu)
Admin (accesses management dashboard)
Display a list of menu items from Firestore, each with:
name, description, image, price, availability
quantity selector with + and - buttons
Cart state is stored locally (e.g., in memory or localStorage)

At the bottom of the page:
Button: “I'm finished ordering” → goes to /checkout
Button: “Cancel” → clears all selections and refreshes page
Displays selected items and total price
Options:
Button: “Self pickup”
Opens modal to input:
Name
Desired pickup time
Show message: “Operating hours: [customizable]”
On submit → create new order in Firestore, redirect to /confirmation
Button: “Home delivery”
Opens modal to input:
Name
Show message: “Home delivery starts at 8:30pm”
On submit → create new order in Firestore, redirect to /confirmation
Button: “Cancel order” → clear selections and redirect to /
Static page:
“Thank you for your business, your order will be attended to soon. Please pay via cash or QR when you arrive at the restaurant, see you soon!”

Display all menu items
Functions:
Add/edit/delete menu items (name, description, price, image URL, availability toggle)
Set availability status
Real-time view of all incoming orders
Each order displays:
Items
Total price
Type: Self pickup / Home delivery
Name
Pickup time (if any)
Timestamp
Ability to mark orders as fulfilled or canceled
Orders sorted by time, newest first
View past orders
Filter by date or type
Optional: Export as CSV
```

Current issues / improvements:
1. Integrating Firestore to store states so menu and orders can be synced across multiple devices. Currently state is only preserved on a single device.
2. Add authetication for accessing the Admin site. Currently anyone can access it via the URL or the link >.<

video src='demo.mov' width=180/>
