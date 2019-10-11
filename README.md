# albelli
Albelli Technical Assignment

Hi there,

Here's my technical assignment.

Thank you for giving me more time, has been a little dificult to get time for this since I'm also taking an 11 weeks course.

I did the web api, a couple of simple test cases and a tried to create a client page for Orders (index.cshtml) and Products (ProductsCatalog.cshtml) so you can see how the api is call but I couldn't finish orders one (index page), anyway api is working, I did a quick test with Postman.

When you run it the api will be loaded with the 5 products described in the document you send me and with one example order so you can just run and us postman or something else to see. You can try with localhost/api/products, localhost/api/products/1, localhost/api/orders, localhost/api/orders/1, etc.

Here's the approach I use.

I use these properties for Products model:
Id = identifier
Name = ProductType or Product name
Width = Product width in mm
MaxStack = How many products of the same kind can be stacked

I use these properties for Orders model:
Id = identifier
Quantity = Product quantity
RequiredBinWidth = Width in mm required to store all the products in the order.

To calculate RequiredBinWidth:
dividing product quantity / MaxStack and return the next integer up.
Example with Mugs.
MaxStack = 4
Quantity = 5
Width = 94 mm

5/4 = 1.25 then the value returned using Math.Ceiling function is 2
2 * 94 mm = 188 mm

Then RequiredBinWidth = 188 mm

Let me know if you have questions.
