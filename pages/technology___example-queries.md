- #+BEGIN_QUERY
  {:title "Pages mentioning [[technology/language/Java]]"
   :query [:find (pull ?page [*])
           :where
           [?page :block/marker ?marker]
  
           [(clojure.string/includes? (clojure.string/lower-case ?page) "technology/language/java")]]
  }
  #+END_QUERY
-
- {{query (and [[technology/language/Java]] [[technology/language/python]] )}}
  query-table:: true
  query-properties:: [:page :block]
- {{query (or [[technology/language/java]] [[technology/testing]]) }}