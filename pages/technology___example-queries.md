- #+BEGIN_QUERY
  {:title
   [[:find (pull ?page [*]) 
     :where 
     [?page :block/marker ?block]
     [?page :block/refs ?java]
     [?page :block/refs ?testing]
     [(clojure.string/includes? ?block "Java")]
     [(clojure.string/includes? ?block "testing")]]}
  #+END_QUERY
-
-
-
- {{query (or [[technology/language/java]] [[technology/testing]]) }}