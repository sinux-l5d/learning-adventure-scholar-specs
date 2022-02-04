
# Proposition de conception base de donnée


## Template :
{**"_id"** : "string",  
**"nom"** : "string",
**"thèmes"**: "string[]",  
**"énoncé"**: "string",  
**"commentaire"**: "string",  
**"auteurs"**: "string[]",  
**"langage"**: "string",  
**"session"**: "string[]",  
**"difficulté"**: "Difficulté",  
**"tempsMoyen"**: "default integer (à définir)",  
**"tempsMaximal"**: "default integer (à définir)};  
,**"dataSet"**: [{"contexte":"string" ,"jeuxdetests" : [{"paramètres": "T[]", "resultat": "U"}]}]  
**"correction"**: "string",  
**"aides"**: "string [] ",   
}  

### -> Types énumérés  
  
Difficulté = {
"facile": 1,
"moyen": 2,
"difficile": 3
}
  
  

## Exemple de document : 

{ **_id**: "5cf0029caff5056591b0ce7d", 
**'nom'** : '1254', 
**‘themes’** : [‘bouclePour ‘,’listes’,’entiers’,’moyenne’],  
**‘enonce’** : ‘ Vous avez n valeurs données en paramètre dans un tableau T. \n
Ecrivez un programme calculant la moyenne de ces valeurs. \n
Exemple : moyenne([1,2,3],3)\n
		→ 2’\n,  
**‘commentaire’** : ‘ Cette fonction calcul la moyenne’,  
**‘auteurs’** : [‘clement’,’romainN’],  
**‘langage’** : ‘C’,  
**‘session’** : [‘L2_403’,'L3_604']  
**‘difficulté’** :’2’,  
**‘tempsmoyen’** :’15’,  
**‘tempsmaxi’** :’40’,  
**‘dataSet’**:[{**'contexte'** : 'default', 
		**'jeuxdetests'** : [{ **'parametres'** :‘[0,0,0,0,0]’, **resultat** :‘0’},
				   {**'parametres‘**:'[1,2,3,4,5,7’]',**'resultat'** :’4’},
				   {**'parametres'**,[-5,0,5,10,15]’, **'resultat'**:’10’}
				   ]
		}],
**‘correction’** : ‘ int moyenne(int[] T,int n){
			int res = 0;
			for (int i =0 ;i<n ;i++) { res += T[i]};
			return res/n ;} ‘,  
**‘aide’**:[‘pour calculer une moyenne il faut parcourir la liste’,’il faudra additionner toutes les valeurs’,’peut etre faut il faire une division à la fin’],}
