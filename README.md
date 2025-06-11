<h1>TP ESLINT</h1>

<h2>Test d'ESLint sur un fichier JavaScript</h2>

Dans le fichier app.js, nous n'observons aucune erreur avec ESLint.

Dans le fichier index.js, nous observons les erreurs suivantes :
```
   7:7   error  'unusedVar' is assigned a value but never used  no-unused-vars
  19:7   error  'message' is assigned a value but never used    no-unused-vars
  21:5   error  Unexpected constant condition                   no-constant-condition
  25:7   error  'tableau' is assigned a value but never used    no-unused-vars
  36:10  error  'toutFaire' is defined but never used           no-unused-vars
  56:7   error  'd' is assigned a value but never used          no-unused-vars
  58:10  error  'fetchData' is defined but never used           no-unused-vars
  63:7   error  'nombres' is assigned a value but never used    no-unused-vars
  67:1   error  Unexpected 'debugger' statement                 no-debugger

✖ 9 problems (9 errors, 0 warnings)
```

En effet, plusieurs variables ont été déclarées mais n'ont pas été utilisé dans le code (unusedVar, message, tableau, toutFaire, d, fetchData, nombres).

Nous avons également une erreur à la 21, où nous avons une condition qui est toujours fausse et ne sera dont jamais exécutée. 

Enfin, nous avons une erreur à la ligne 67, où nous retrouvons l'instruction debugger. Cette instruction utilisé lors du développement risque de créer des problèmes d'exécution du script en production. Nous pouvons commenter cette ligne.

Afin de régler cela, nous pouvons supprimer les instructions qui ne seront jamais exécutés, afficher les variables déclarées et non utilisées dans la console ainsi que les tests de debug.