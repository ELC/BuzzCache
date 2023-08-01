- #+BEGIN_QUERY
  {
   :query [:find ?title
   :where
   [?page :block/string ?title]
   [?title :find/text "technology/language/Java"]
  
  ]
  #+END_QUERY
-
- {{query (and [[technology/language/Java]] [[technology/language/python]] )}}
  query-table:: true
  query-properties:: [:page :block]
- {{query (or [[technology/language/java]] [[technology/testing]]) }}