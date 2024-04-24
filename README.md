# jaxbxjc


using the @XmlType annotation we can specify the order in which these fields should be serialized 
when they are converted into xml.by default in whichever order they are defined in the xml the same is used here.
All the fields get generated in the same order.

@XmlRootElement(name = "patient") this tells that the root element for an object of this class when it is
serialized into xml should be the following name is equal to patient.


@XmlAccessorType(XmlAccessType.FIELD)  annotation again is used at the class level,
Here we are specifying whether all the annotations inside the class are at a field level or at a method
level.And in this case they are all at field level by default.
You can also have these annotations at the setter and getter method level for these fields.

 @XmlElement  tells us that each of these fields on this object should be converted into a xml element of its
own when the object gets serialized and 
when it gets deserialized from the xml Each of the elements should be mapped to the appropriate field here.
By default the name of the xml elements will be the name of the fields here.But we can customize that 
by using this XML element inside of this you can specify a name as well.

@XmlAttribute tells that this ID field should not be an element but
should be an attribute on the patient object that is because 
in the schema if you notice ID is an
attribute that is why automatically when the stubs got generated it looks at that in the schema and
then it uses the appropriate annotation 