# # Teach Arduino to my Dad

## Pourquoi ce dépôt ?

Ce dépôt est à destination de mon père (et potentiellement de tous les pères du monde) qui souhaite apprendre à programmer. Je lui rédige donc des exercices court, didactiques, accompagnés d'exemples lui permettant d'apprendre Arduino par la pratique.

## Memo

### Modèle de fichier

```C
void setup() {
  // Cette fonction n'est exécutée qu'une seule fois
  // Elle doit permettre d'initialiser toutes les variables, toutes les entrées et toutes les sorties
}

void loop() {
  // Cette fonction est exécutée en boucle et ne se termine jamais
}
```

### Déclaration de variables

Une variable possède trois caractéristiques : un type, un nom et une valeur
- Le type décrit ce que contiendra la variable : un nombre, des caractères, un booléen, etc.
- Le nom de la variable est fixe et servira à rappeler la variable pour écrire ou lire une valeur dans celle-ci
- La valeur est stockée en mémoire et peut changer au fur et à mesure de l'exécution du programme. On peut lire et écrire cette valeur

#### Types de variables

| Type          | Contenu           | Bornes  | Exemple  |
| ------------- |:-----------------:| -------:| --------:|
| char          | Un caractère | Tout caractère alphanumérique | `char c = 'A'`
| byte          | Un nombre | De 0 à 255 | `byte b = 12`
| int          | Un nombre | De -32,768 to 32,767 | `int i = 12345`
| long          | Un nombre | De -2,147,483,648 à 2,147,483,647 | `long i = 1234567890`
| float          | Un nombre à virgule | De -3.4028235E+38 à 3.4028235E+38 | `long i = 123.456`
| double          | Un nombre à virgule | De -3.4028235E+38 à 3.4028235E+38 | `long i = 123.456`

#### Nom de variable

Le nom d'une variable doit indiquer à quoi sert cette variable. On ne déclare pas une variable `a` mais une variable `led1` par exemple

#### Affectation d'une variable

Pour affecter une variable, on utilise le caractère `=`

### Bloc de code

Un bloc de code est déclaré à l'aide de `{ }`, il contient un ensemble de lignes de code qui seront exécutées à la suite sans interruption possible.

```C
{
    // Ceci est un bloc de code dont chaque ligne sera exécutée
    // Ligne 1
    // Ligne 2
    // Ligne 3
}
```

### Condition

Une condition s'écrit avec le mot clé `if` et permet d'exécuter un bloc de code si et seulement si la condition est respectée

```C
int maVariableA = 2;

if (maVariableA == 2) {
    // Si maVariableA est égale à 2, alors on exécute ce bloc
}
```

#### Comparaison

Pour comparer une variable à une valeur (demander si une variables est égale à une valeur par exemple), on utilise les opérateurs

| Opérateur          | Test           | Exemple  |
| ------------- |:-----------------:| --------:|
| ==          | Si la valeur est égale à | `if (variable == 1)`
| !=          | Si la valeur est différente de | `if (variable != 1)`
| <          | Si la valeur est inférieure à | `if (variable < 1)`
| >          | Si la valeur est supérieure à | `if (variable > 1)`
| <=          | Si la valeur est inférieure à OU égale à | `if (variable <= 1)`
| >=          | Si la valeur est supérieure à OU égale à | `if (variable >= 1)`

#### Opérateur ET

Si une condition doit faire plusieurs tests d'un coup, il est possible d'utiliser l'opérateur ET qui s'écrit `&&`

```C
int maVariableA = 2;
int maVariableB = 3;

if (maVariableA == 2 && maVariableB == 3) {
    // Si maVariableA est égale à 2 ET si maVariableB est égale à 5, alors on exécute ce bloc
}
```

#### Opérateur OU

Si une condition doit faire plusieurs tests d'un coup, il est possible d'utiliser l'opérateur OU qui s'écrit `||`

```C
int maVariableA = 2;
int maVariableB = 3;

if (maVariableA == 2 || maVariableA == 5) {
    // Si maVariableA est égale à 2 OU si maVariableB est égale à 5, alors on exécute ce bloc
}
```

#### Condition sinon

Lorsqu'une condition n'est pas respectée, il est possible d'écrire un bloc de code qui sera exécuté à la place du bloc qui aurait dû être exécuté si la condition avait été respectée. Il s'agit du mot clé `else`

```C
int maVariable = 2;

if (maVariable == 3) {
    // S'exécute si la variable est égale à 3
} else {
    // S'exécute si la variable est différente de 3
}
```