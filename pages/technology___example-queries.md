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
  		:find (pull ?b [*]) 
  		:where 
  			[?b :block/uuid] 
  			[?b :block/marker ?marker] 
  			[(contains? *#{"TODO" "DOING" "LATER" "NOW"} ?marker)] *
  	]
  }
  #+END_QUERY
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