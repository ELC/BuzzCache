- #+BEGIN_QUERY
  {:title
   [[:find (pull ?page [*]) 
     :where 
     [?page :block/refs ?technology]
  #+END_QUERY
- query-sort-by:: page
  query-table:: false
  query-sort-desc:: true
  query-properties:: [:page]
  #+BEGIN_QUERY
  {
  	:query [
  		:find (pull ?p [*]) 
  		:where 
              [?p :block/refs ?technology/language/Java]
  	]
  }
  #+END_QUERY
-
- #+BEGIN_QUERY
  {
   :query [:find (pull ?page [*])
   :where
   [?page :page/marker ?page]
   [?page :page/refs ?java]
   
   [(clojure.string/includes? ?page"Java")]
   
  ]
  }
  #+END_QUERY
-
-
- {{query (or [[technology/language/java]] [[technology/testing]]) }}