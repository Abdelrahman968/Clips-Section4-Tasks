         CLIPS (6.30 3/17/15)
CLIPS> (deftemplate person
   (multislot name 
      (type SYMBOL STRING)
      (cardinality 2 4))
   (slot age 
      (type INTEGER)
      (range 20 25))
)
CLIPS> (deffacts people
   (person (name Abdelrahmna Ayman) (age 22))
   (person (name Ahmed Elsayed) (age 24))
   (person (name Tark Ebrahim) (age 21))
)
CLIPS> (defrule check_age
   (person (name $?n) (age ?a&:(and (> ?a 20) (<= ?a 25))))
   =>
   (printout t ?n " is between 20 and 25 years old." crlf)
)
CLIPS> (reset)
CLIPS> (facts)
f-0     (initial-fact)
f-1     (person (name Abdelrahmna Ayman) (age 22))
f-2     (person (name Ahmed Elsayed) (age 24))
f-3     (person (name Tark Ebrahim) (age 21))
For a total of 4 facts.
CLIPS> (run)
(Tark Ebrahim) is between 20 and 25 years old.
(Ahmed Elsayed) is between 20 and 25 years old.
(Abdelrahmna Ayman) is between 20 and 25 years old.
CLIPS> 
