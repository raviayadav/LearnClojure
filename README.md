# LearnClojure

```clj
(defn petToHumanAge
  "This function returns human to pet years"
  [x]
  (def petStore {'dog 7 'cat 5 'goldfish 10})
  (get petStore x))

(defn age
  "This function returns age of pets"
  [petName petType petAge]
  (def ratio (petToHumanAge petType))
  (println petName "is" (* petAge ratio) "years old in human years"))

(age "Fido" 'dog 4)
```
