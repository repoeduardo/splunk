# BEST PRACTICES ON SEARCHING

1 - time is the most efficient filter

2 - specify two or more index values in the beggining of the search

~~~spl
(index="windows" OR index="main") sourcetype="xmlwineventlog"
~~~

3 - include as many search terms as possible

4 - be more specific as much you can when searching, include double quotes ""

~~~spl
index="main" host="VM-DSK-WIN10" sourcetype=XmlWinEventLog subject="An account was successfully logged on"
~~~

5 - inclusion is generally better than exclusion

6 - Avoid using wildcards

7 - When possible, use OR instead of wildcards

