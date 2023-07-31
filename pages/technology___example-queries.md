- #+BEGIN_QUERY
  {:title
   [[:find (pull ?page [*]) 
     :where 
     [?page :block/refs ?technology]
  #+END_QUERY
- {{and [[Java]] [[testing]]}}
-
-
-
- {{query (or [[technology/language/java]] [[technology/testing]]) }}