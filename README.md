# Bank-Account
Gestionnaire Compte Bancaire

class ComptesBancaires{
  constructor(titulaire, solde){
    this.titulaire=titulaire;
    this.solde=0;
  }
  crediter(montant){
    this.solde+=montant;
  }
  decrire(){
    return `${this.titulaire} a un solde de ${this.solde} euros dans son compte !`;
  }
}

const listeComptes = [];

listeComptes.push (new ComptesBancaires("Alex"));
listeComptes.push (new ComptesBancaires("Clovis"));
listeComptes.push (new ComptesBancaires("Marco"));


for (var i=0; i<listeComptes.length; i++)
  {
    console.log(listeComptes[i].decrire());
  }

for (var i=0; i<listeComptes.length; i++)
  {
    listeComptes[i].crediter(1000);
    console.log(listeComptes[i].decrire());
  }
