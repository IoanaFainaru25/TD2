# TD2
Devoir - TD 2 pour ALF



public $validate = array(


    'numero_cc' => array(
    
        'rule' => array('cc', array('visa', 'maestro'), false, null),
        
        'message' => 'Le numéro de carte de crédit que vous avez saisi était invalide.'
        
    )
    
);





    Validation::cc(mixed $check, mixed $type = 'fast', boolean $deep = false, string $regex = null)¶
Cette règle est utilisée pour vérifier si une donnée est un numéro de carte de crédit valide. Elle prend trois paramètres : ‘type’, ‘deep’ et ‘regex’.

Le paramètre ‘type’ peut être assigné aux valeurs ‘fast’, ‘all’ ou à l’une des suivantes :

-amex
-bankcard
-diners
-disc
-electron
-enroute
-jcb
-maestro
-switch
-visa
-voyager

  Si ‘type’ est défini à ‘fast’, cela valide les données de la majorité des formats numériques de cartes de crédits. Définir ‘type’ à ‘all’ vérifiera tous les types de cartes de crédits. Vous pouvez aussi définir ‘type’ comme un tableau des types que vous voulez détecter.

  Le paramètre ‘deep’ devrait être défini comme une valeur booléenne. S’il est défini à true, la validation vérifiera l’algorithme Luhn de la carte de crédit (http://en.wikipedia.org/wiki/Luhn_algorithm). Par défaut, elle est à false.

  Le paramètre ‘regex’ vous permet de passer votre propre expression régulière, laquelle sera utilisée pour valider le numéro de la carte de crédit:
