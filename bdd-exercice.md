
# Proposition de conception base de donnée

## Template :
{**"_id"** : "string",  
**"nom"** : "string",  
**"themes"**: "string[]",  
**"enonce"**: "string",  
**"template"**: "string",  
**"commentaire"**: "string",  
**"auteurs"**: "string[]",  
**"langage"**: "string",  
**"session"**: "string[]",  
**"difficulte"**: "integer",  
**"tempsMoyen"**: "default integer (à définir)",  
**"tempsMaximum"**: "default integer (à définir)",   
,**"dataSet"**: [{"contexte":"string" ,"jeuxdetests" : [{"paramètres": "string[]", "resultat": "string"}]}],  
**"correction"**: "string",  
**"aides"**: "string [] ",  
}  


  

## Exemple de document : 

{ **_id**: "5cf0029caff5056591b0ce7d", 
**"nom"** : "1254", 
**"themes"** : ["bouclePour","listes","entiers","moyenne"],  
**"enonce"** : "Vous avez n valeurs données en paramètre dans un tableau T. \n
Ecrivez un programme calculant la moyenne de ces valeurs. \n
Exemple : moyenne([1,2,3],3)\n
		→ 2\n",
**"template"**:"",  
**"commentaire"** : " Cette fonction calcul la moyenne",  
**"auteurs"** : ["clement","romainN"],  
**"langage"** : "C",  
**"session"** : ["L2_403","L3_604"],
**"difficulte"** :"2",  
**"tempsMoyen"** :"15",  
**"tempsMaximum"** :"40",  
**"dataSet"**:[{**"contexte"** : "default", 
		**"jeuxdetests"** : [{ **"parametres"** :"[0,0,0,0,0]", **"resultat** :"0"},
				   {**"parametres"**:"[1,2,3,4,5,7]",**"resultat"** :"4"},
				   {**"parametres"**,:"[-5,0,5,10,15]", **"resultat"**:"10"}
				   ]
		}],  
**"correction"** : " int moyenne(int[] T,int n){
			int res = 0;
			for (int i =0 ;i<n ;i++) { res += T[i]};
			return res/n ;} ",  
**"aide"**:["pour calculer une moyenne il faut parcourir la liste","il faudra additionner toutes les valeurs","peut etre faut il faire une division à la fin"],
}
