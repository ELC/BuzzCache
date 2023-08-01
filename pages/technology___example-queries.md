- #+BEGIN_QUERY
  {
   :query [:find ?page
   :where
   [?page :page/name ?page-name]
   [(clojure.string/includes? ?page-name "technology/language/Java")]]
  ]
  #+END_QUERY
-
- {{query (and [[technology/language/Java]] [[technology/language/python]] )}}
  query-table:: true
  query-properties:: [:page :block]
- {{query (or [[technology/language/java]] [[technology/testing]]) }}