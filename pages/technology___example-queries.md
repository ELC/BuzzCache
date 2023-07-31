- #+BEGIN_QUERY
  {:title
   [[:find (pull ?page [*]) 
     :where 
     [?page :block/refs ?technology]
  #+END_QUERY
- {
   :title [:h2 "🧨 OVERDUE"]
   :query [
           :find (pull ?b [*])
           :in $ ?start ?today
           :where
           (between ?b ?start ?today)
           (task ?b #{"TODO" "DOING"})
           (not [?b :block/scheduled])
           (not [?b :block/priority "A"])
          ]
   :inputs [:-180d :today]
   :breadcrumb-show? true
  }
-
-
- {{query (or [[technology/language/java]] [[technology/testing]]) }}