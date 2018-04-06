# Test-Unitaire

Ce tp, basé sur l'exemple d'un code barre d'un produit,
aide à manipuler les *tests unitaires*

Un test unitaire va permettre de créer un programme qui va tester l'ensemble des méthodes d'une classe. Si l'on doit effectuer une maintenance évolutive ou corrective on pourra rejouer cette séance de code de test afin de valider que la classe fonctionne toujours correctement.
Dans le système d'identification des produits par code barre, un code est une succession de 12 chiffres. Il est complété d'un treizième chiffre appelé *clé de code* qui sert à la vérification de la bonne saisie du code. Le but est de générer un programme qui à partir des 12 chiffres d'un code barre, calcule la clé de contrôle et vérifie qu'il n'y pas d'erreur de saisie.


### Exemple du code de la méthode Test pour la génération de la clé
        /// <summary>
        ///Test pour Cle
        ///</summary>
        [TestMethod()]
        public void CleTest()
        {
            //int[] ean13 = null; // TODO: initialisez à une valeur appropriée
            Ean13 target = new Ean13(new int[] { 4, 7, 1, 9, 5, 1, 2, 0, 0, 2, 8, 8}); // TODO: initialisez à une valeur appropriée
            int expected = 9; // TODO: initialisez à une valeur appropriée
            int actual;
            actual = target.Cle();
            Assert.AreEqual(expected, actual);
        }
        
### Le résultat des tests est affiché ici pour chaque méthode

![Capturegencode.png](https://github.com/meloeenazaire/Test-Unitaire/blob/master/Capturegencode.PNG)
