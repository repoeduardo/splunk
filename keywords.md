# KEYWORDS


## BOOLEAN OPERATORS

and, not, or

``and`` -> this operator is implicit, which means if you put a space between two words in search bar then splunk automatically will consider this search with `and` operator.

For example, this:

~~~txt
index="main" sourcetype="access_combined_wcookie" buttercupgames Chrome
~~~

is the same thing of this:

~~~txt
index="main" AND sourcetype="access_combined_wcookie" AND buttercupgames AND Chrome
~~~

<hr>

`not` -> the "not" operator, also known as logical negation, inverts the truth value of a boolean expression. If the expression is true, "not" makes it false, and vice versa

For example:

~~~txt
index="main" AND sourcetype="access_combined_wcookie" NOT action="remove" OR action="view"
~~~

with this search Splunk bring to us all events where `action` field is not equal to "remove" and not equal to "view"

<hr>

`or` -> this operator evaluates to true if at least one of its conditions is true.

For example:

~~~txt
index="main" AND sourcetype="access_combined_wcookie" AND action="remove" OR action="view"
~~~

with this search Splunk bring to us all events where `action` field is equal to "remove" or equal to "view"