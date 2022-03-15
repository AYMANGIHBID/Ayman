#pragma once
#include "CompteEpargne.h"
#include "ComptePayant.h"
#include "Devise.h"
#include<iostream>
using namespace std;
class CpEpargne_pay : public CompteEpargne, public ComptePayant
{

public:
	CpEpargne_pay(Client* c, Devise*d, double taux);
	bool retirerArgent(Devise montant)override;
	void deposerArgent(Devise montant)override;
	~CpEpargne_pay();


};
  #include "CpEpargne_pay.h"

CpEpargne_pay::CpEpargne_pay(Client* c, Devise* d, double taux):
	CompteEpargne(c,d,taux), Compte(c,d);
{
}

bool CpEpargne_pay::retirerArgent(Devise montant){



}

void CpEpargne_pay::deposerArgent(Devise montant)
 {


 }


CpEpargne_pay::~CpEpargne_pay()
{
}
