- #+BEGIN_QUERY
  {
   :query [
  :find (pull ?p [*])
  ]
  ]
  #+END_QUERY
-
- {{query (and [[technology/language/Java]] [[technology/language/python]] )}}
  query-table:: true
  query-properties:: [:page :block]
- {{query (or [[technology/language/java]] [[technology/testing]]) }}