pizzapy
Disclaimer
This is my fork of https://github.com/gamagori/pizzapi It's heavily modified and not well documented, but i'm going to get to that. the below example should work though.

sorry! was kind of in a rush this morning.

Setup
pizzapy
Disclaimer
This is my fork of https://github.com/gamagori/pizzapi It's heavily modified and not well documented, but i'm going to get to that. the below example should work though.

sorry! was kind of in a rush this morning.

Setup
pizzapy
Disclaimer
This is my fork of https://github.com/gamagori/pizzapi It's heavily modified and not well documented, but i'm going to get to that. the below example should work though.

sorry! was kind of in a rush this morning.

Setup
1.install python3
2.download this repository
3.Unzip/extract the .rar
4.install the requirements of the repository `pip install -r (filepath of quirements.txt)` (yes you do neeed to specify the file path of the requirements)
5.in the "Use this interpreter" interpreter already placed in the pizzapi-master folder, type 'from pizzapy import *' and everything else that Jarvis is typing in the video. https://www.youtube.com/watch?v=Nxu6GlDleqA
6.have fun
Description
This is a Python wrapper for the Dominos Pizza API.

It's a port of the pizzapi node.js module written by RIAEvangelist.

Quick Start
First construct a Customer object and set the customer's address:

customer = Customer('Barack', 'Obama', 'barack@whitehouse.gov', '2024561111', '700 Pennsylvania Avenue NW, Washington, DC, 20408')
Then, find a store that will deliver to the address.

my_local_dominos = StoreLocator.find_closest_store_to_customer(customer)
In order to add items to your order, you'll need the items' product codes. To find the codes, get the menu from the store, then search for items you want to add. You can do this by asking your Store object for its Menu.

menu = my_local_dominos.get_menu()
Then search menu with menu.search. For example, running this command:

menu.search(Name='Coke')
Should print this to the console:

20BCOKE    20oz Bottle Coke®        $1.89
20BDCOKE   20oz Bottle Diet Coke®   $1.89
D20BZRO    20oz Bottle Coke Zero™   $1.89
2LDCOKE    2-Liter Diet Coke®       $2.99
2LCOKE     2-Liter Coke®            $2.99
After you've found your items' product codes, you can create an Order object add add your items:

order = Order.begin_customer_order(customer, my_local_dominos)
order.add_item('P12IPAZA') # add a 12-inch pan pizza
order.add_item('MARINARA') # with an extra marinara cup
order.add_item('20BCOKE')  # and a 20oz bottle of coke
You can remove items as well!

order.remove_item('20BCOKE')
Wrap your credit card information in a CreditCard:

card = CreditCard('4100123422343234', '0115', '777', '90210')
And that's it! Now you can place your order.

order.place(card)
my_local_dominos.place_order(order, card)
Description
This is a Python wrapper for the Dominos Pizza API.

It's a port of the pizzapi node.js module written by RIAEvangelist.

Quick Start
First construct a Customer object and set the customer's address:

customer = Customer('Barack', 'Obama', 'barack@whitehouse.gov', '2024561111', '700 Pennsylvania Avenue NW, Washington, DC, 20408')
Then, find a store that will deliver to the address.

my_local_dominos = StoreLocator.find_closest_store_to_customer(customer)
In order to add items to your order, you'll need the items' product codes. To find the codes, get the menu from the store, then search for items you want to add. You can do this by asking your Store object for its Menu.

menu = my_local_dominos.get_menu()
Then search menu with menu.search. For example, running this command:

menu.search(Name='Coke')
Should print this to the console:

20BCOKE    20oz Bottle Coke®        $1.89
20BDCOKE   20oz Bottle Diet Coke®   $1.89
D20BZRO    20oz Bottle Coke Zero™   $1.89
2LDCOKE    2-Liter Diet Coke®       $2.99
2LCOKE     2-Liter Coke®            $2.99
After you've found your items' product codes, you can create an Order object add add your items:

order = Order.begin_customer_order(customer, my_local_dominos)
order.add_item('P12IPAZA') # add a 12-inch pan pizza
order.add_item('MARINARA') # with an extra marinara cup
order.add_item('20BCOKE')  # and a 20oz bottle of coke
You can remove items as well!

order.remove_item('20BCOKE')
Wrap your credit card information in a CreditCard:

card = CreditCard('4100123422343234', '0115', '777', '90210')
And that's it! Now you can place your order.

order.place(card)
my_local_dominos.place_order(order, card)
Description
This is a Python wrapper for the Dominos Pizza API.

It's a port of the pizzapi node.js module written by RIAEvangelist.

Quick Start
First construct a Customer object and set the customer's address:

customer = Customer('Barack', 'Obama', 'barack@whitehouse.gov', '2024561111', '700 Pennsylvania Avenue NW, Washington, DC, 20408')
Then, find a store that will deliver to the address.

my_local_dominos = StoreLocator.find_closest_store_to_customer(customer)
In order to add items to your order, you'll need the items' product codes. To find the codes, get the menu from the store, then search for items you want to add. You can do this by asking your Store object for its Menu.

menu = my_local_dominos.get_menu()
Then search menu with menu.search. For example, running this command:

menu.search(Name='Coke')
Should print this to the console:

20BCOKE    20oz Bottle Coke®        $1.89
20BDCOKE   20oz Bottle Diet Coke®   $1.89
D20BZRO    20oz Bottle Coke Zero™   $1.89
2LDCOKE    2-Liter Diet Coke®       $2.99
2LCOKE     2-Liter Coke®            $2.99
After you've found your items' product codes, you can create an Order object add add your items:

order = Order.begin_customer_order(customer, my_local_dominos)
order.add_item('P12IPAZA') # add a 12-inch pan pizza
order.add_item('MARINARA') # with an extra marinara cup
order.add_item('20BCOKE')  # and a 20oz bottle of coke
You can remove items as well!

order.remove_item('20BCOKE')
Wrap your credit card information in a CreditCard:

card = CreditCard('4100123422343234', '0115', '777', '90210')
And that's it! Now you can place your order.

order.place(card)
my_local_dominos.place_order(order, card)
