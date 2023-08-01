- #+BEGIN_QUERY
  {:title "Pages mentioning [[technology/language/Java]]"
   :query [:find ?page
           :where [?page :block/marker "technology/language/Java"]
  ]
  #+END_QUERY
-
- {{query (and [[technology/language/Java]] [[technology/language/python]] )}}
  query-table:: true
  query-properties:: [:page :block]
- {{query (or [[technology/language/java]] [[technology/testing]]) }}