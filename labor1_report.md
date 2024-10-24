<p align="center"><b>МОНУ НТУУ КПІ ім. Ігоря Сікорського ФПМ СПіСКС</b></p>
<p align="center">
<b>Звіт з лабораторної роботи 1</b><br/>
"Обробка списків з використанням базових функцій"<br/>
дисципліни "Вступ до функціонального програмування"
</p>
<p align="right"><strong>Студент:</strong> Ольховський Максим Олександрович КВ-13 </p>
<p align="right"><strong>Рік:</strong> 2024</p>

## Загальне завдання

```lisp
(setq personal-list          ; task 1
(list
'laboratorna            ; at least one symbol 
28                 ; at least one number
(list 'number 2 8) ; at least one non-empty sublist        
'()                ; at least one empty sublist
(cons 'f 'g)))     ; another sublist


CL-USER> (car personal-list) ; task 2
LABORATORNA

CL-USER> (cdr personal-list) ; task 3
(28 (NUMBER 2 8) NIL (F . G))

CL-USER> (nth 2 personal-list) ; task 4
(NUMBER 2 8)

CL-USER> (last personal-list) ; task 5
((F . G))

CL-USER> (atom (first personal-list)) ; task 6
T
CL-USER> (atom (second personal-list))
T
CL-USER> (atom (last personal-list))
NIL
CL-USER> (listp (first personal-list))
NIL
CL-USER> (listp (third personal-list))
T
CL-USER> (listp (last personal-list))
T
CL-USER> (equalp (first personal-list) (last personal-list)) ; task 7
NIL
CL-USER> (numberp (first personal-list))
NIL
CL-USER> (numberp (second personal-list))
T
CL-USER> (append personal-list (second personal-list)) ; task 8
(LABORATORNA 28 (NUMBER 2 8) NIL (F . G) . 28)
```

## Варіант 12(4)

<p align="center">
<img src="labor1_var.jpg">
</p>

```lisp
(let ((var '(A)))  
  (list (cons 1 var)
         (cons 2 var)
         (cons 3 var)
         'C))

((1 A) (2 A) (3 A) C)
```
