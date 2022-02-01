<?xml version="1.0" encoding="EUC-JP" standalone = 'yes'?>

<schema xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.LanceMendoza.com/NewXMLSchema"
	xmlns:tns="http://www.LanceMendoza.com/NewXMLSchema"
	elementFormDefault="qualified">

</schema>

















---------------------------------------------------------------------------
<!-- These are notes for the specific section -->

W3S

XML Schema definition

Grammar or blueprint of the XML document: XMl follows XSD (XML Schema Definition = .xsd externsion) is valid document.

		Elements
		Attributes
		Namespaces
		Order
		Number of occurrence
		Restrictions

XML Schema defines what what can be included in the XML document.

	Order.xml Order.xsd

XML Schema contract between users.
	XML Schema tells us what we can include inside the configuration file.
	XML valid Data we need XML Schema definition.

XML schema types
	Inbuilt types
		int
		decimal
		string
		date
		datetime

	Simple types
		restrict string to 15 characters example.
		<element name = "name" type = "String15Chars"/>
	
	Complex types
		inbuilt types
		simple types
		complex types
	Similar to classes in object programming.

Once elements are marked, those elements/attributes can only carry those types of values within XML document.

Number types:
	bytes - A signed 8 bit integer
	short - 16 bit
	int - 32 bit
	long - 64 bit
	decimal - decimal values (0.1, 0.3, etc.)
	unsignedByte etc - 
Date types:
	date - defines a date value
	dateTime - defines a date and time value
	time - defines a time value
	gDay,Gmonth, etc.
String types:
	string- alpha characters

Example: 
Name - string
Age - int
Email - string
Gender - string
Phone - string

Schema:
	targetNamespace: 
		http://www.amazon.com/order
		http://www.ebay.com/order
Instead of using targetNamespace to qualify you can use Prefix.
	prefix:
		xmlns:amz="http://www.amazon.com/order"
		xmlns:ebay="http://www.ebay.com/order"
			(amz, ebay, url can be anything)

	<order xmlns:amz="http://www.amazon.com/order">
		<amz:lineitem/>
		<amz:shippingaddress/>

	<order xmlns:ebay="http://www.ebay.com/order">
		<ebay:lineitem/>
		<ebay:shippingaddress/>


If we have to use multiple orders from Ebay and amazon in a single XML document looking at the namespace we can tell
the difference.
 
Namespaces allow us to uniquely identify the elements and attributes in a XML document.
We create target namespaces in the schema file which tells that all elements in that schema file should follow
certain namespace and then instead of using the entire URL to qualify each element in the on the schema we use 
prefix.


---------------------------
---------------------------


<?xml version="1.0" encoding="UTF-8"?>
<schema xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.LanceMendoza.com/NewXMLSchema"
	xmlns:tns="http://www.LanceMendoza.com/NewXMLSchema"
	elementFormDefault="qualified">

</schema>

XML schemae File - starts with a declaration by default
schema - Then the root element
xmlns - stands for XML namespace
tns - stands for target namespace

