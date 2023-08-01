- #+BEGIN_QUERY
  {:title "Pages mentioning [[technology/language/Java]]"
   :query [:find (pull ?page [*])
      :where
   [?page :page/name]
   [?page :block/ref-pages ?ref-page]
   [?ref-page :block/string ?mention]
   [(clojure.string/includes? ?mention "technology/language/Java")]
  ]
  #+END_QUERY
-
- {{query (and [[technology/language/Java]] [[technology/language/python]] )}}
  query-table:: true
  query-properties:: [:page :block]
- {{query (or [[technology/language/java]] [[technology/testing]]) }}