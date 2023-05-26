# LearnClojure

### Basic Functions
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
### Conditionals
```clj
(defn ifCond
  []
  (if (= 5 5)
  (println "It's true")
  (println "It's false"))
)

(ifCond)

(defn ifDoCond
  []
  (if (= 5 6)
    (do(println "First Equal Statement")
      (println "Second equal Statement"))
    (do(println "First not equal statement")
      (println "Second not equal statement"))
  )
)

(ifDoCond)

(defn nestedIfCond
  []
  (println "\nNested ifs: ")
  (if (and (= 5 5) (or (= 2 2) (not true)))
    (println "This is true")
    (println "This is false")
  )
)
(nestedIfCond)

(defn condCase
  [pet]
  (println "\n Switch case")
  (case pet
    "dog" (println "It's a dog")
    "cat" (println "It's a cat")
    "monkey" (println "It's a monkey")
    )
  )
(condCase "dog")

(defn condCond
  [amount]
  (println "\nCondCond:")
  (cond
    (<= amount 2) (println "Few")
    (<= amount 10) (println "Several")
    (<= amount 100) (println "Many")
    :else (println "Plenty")
  )
)

(condCond 120)
```
### Loops
```clj
(defn Loop
  []
  (println "/nLoop:")
  (loop [x 0]
    (when (< x 10)
      (println x)
      (recur (inc x))
    )
  )
)

(Loop)

(defn DoTimes
  []
  (println "\n DoTimes Loop:")
  (dotimes [x 10]
    (println x)  
  )
)

(DoTimes)

(defn WhileDo
  [count]
  (println "\n WhileDo loop:")
  (def x (atom 0))
  (while (< @x count)
    (do
      (println "This is the")
      (println "Count:" @x)
      (swap! x inc)
    )
  )
)

(WhileDo 12)

(defn DoSeq
  [seq]
  (println "/nDo Seq:")
  (doseq [x seq]
    (println (inc x))
  )
)

(DoSeq[1 2 3 4 5])
```
