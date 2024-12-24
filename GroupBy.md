# GROUP BY

### Contare quanti iscritti ci sono stati ogni anno

```SQL
SELECT COUNT(*) AS `total`, YEAR(`enrolment_date`) AS `year`
FROM `students`
GROUP BY `year`
```

### Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```SQL
SELECT COUNT(*) AS `total`, `office_address`
FROM `teachers`
GROUP BY `office_address`
```

### Calcolare la media dei voti di ogni appello d'esame

```SQL
SELECT AVG(`vote`) AS `avg`, `exam_id`
FROM `exam_student`
GROUP BY `exam_id`
```

### Contare quanti corsi di laurea ci sono per ogni dipartimento

```SQL
SELECT `department_id`, COUNT(*) AS `num_of_degrees`
FROM `degrees`
GROUP BY `department_id`
```