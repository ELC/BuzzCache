- #+BEGIN_QUERY
  {:title
   [[:find (pull ?page [*]) 
     :where 
     [?page :block/refs ?technology]
  #+END_QUERY
- {{query page [[technology/language/python]]  }}
-
- *#+BEGIN_QUERY*
  {:title "Pages created past 30 days"
   :query [:find (pull ?p [*]) 
           :in $ ?end
           :where
           [?p :block/name _]
           [?p :block/created-at ?t]
           [(- ?end 2629800000) ?start]
           [(>= ?t ?start)]
           [(< ?t ?end)]]
   :inputs [:end-of-today-ms]}
  *#+END_QUERY*
-
-
- {{query (or [[technology/language/java]] [[technology/testing]]) }}