# Koerperberechnungen
#include <iostream>
#include <cmath>
using namespace std;

int main(){
    string koerper;

    string berechnung;
    double volumen;
    double oberflaeche;
    double kantenlaenge;

    double kantenlaenge_a;
    double kantenlaenge_b;
    double kantenlaenge_c;
    double hoehe;
    double radius;
    double mantelflaeche;

   /* string wuerfel;
    string rechtecksaeule;
    string kegel;
    string qu_pyramide;*/

    cout << "Waehlen Sie einen Koerper aus folgender Liste aus \n kugel\n wuerfel\n rechtecksaeule\n kegel\n qu_pyramide\n";
    cout << "\nGeben Sie zum Auswaehlen eines Koerpers den jeweiligen Namen ein: ";

    cin >> koerper;

            //KUGEL
            if (koerper == "kugel"){
                cout << "\nSie haben die kugel gewaehlt\n";

                cout << "\nWas moechten Sie berechnen?\nvolumen\noberflaeche\n";
                cout << "Geben Sie zum Auswaehlen einer Berechnung den jeweiligen Namen ein: ";
                cin >> berechnung;
                //VOLUMEN
                if (berechnung == "volumen"){
                    cout << "\nGeben Sie den Radius der Kugel in Zentimeter ein: ";
                    cin >> radius;


                    volumen = M_PI * (4/3) * pow(radius,3);
                    //spuckt hier scheinbar falsches Ergebnis aus
                    cout << "\nDas Volumen des Koerpers betraegt: " << volumen << "cm^3";
                        return 0;
                }
                //OBERFLAECHE
                else if (berechnung == "oberflaeche"){
                   cout << "\nGeben Sie den Radius der Kugel in Zentimeter ein: ";
                   cin >> radius;

                   oberflaeche = 4 * M_PI * pow(radius,2);
                   cout << "\nDie Oberflaeche des Koerpers betraegt: " << oberflaeche << "cm^2";
                        return 0;
                }
                //FEHLERMELDUNG BEZEICHNUNG
                else {
                    cout << "Bitte geben Sie eine korrekte Berechnungsbezeichnung ein!";
                        return 0;
                }

            }

            //WUERFEL
            else if (koerper == "wuerfel"){
                cout << "\nSie haben den wuerfel gewaehlt";

                cout << "\nWas moechten Sie berechnen?\nvolumen\noberflaeche\n";
                cout << "Geben Sie zum Auswaehlen einer Berechnung den jeweiligen Namen ein: ";
                cin >> berechnung;

                //VOLUMEN
                if (berechnung == "volumen"){
                cout << "\nGeben Sie die Kantenlaenge des Wuerfels in Zentimeter ein: ";
                cin >> kantenlaenge_a;

                    volumen = pow(kantenlaenge_a,3);
                    cout << "\nDas Volumen des Koerpers betraegt: " << volumen << "cm^3";
                        return 0;
                }
                //OBERFLAECHE
                else if (berechnung == "oberflaeche"){
                   cout << "\nGeben Sie die Kantenlaenge des Wuerfels in Zentimeter ein: ";
                   cin >> kantenlaenge_a;

                   oberflaeche = kantenlaenge_a * kantenlaenge_a * 6;
                   cout << "\nDie Oberflaeche des Koerpers betraegt: " << oberflaeche << "cm^2";
                    return 0;
                }

                //FEHLERMELDUNG EINGABE
                else {
                    cout << "Bitte geben Sie eine korrekte Berechnungsbezeichnung ein!";
                    return 0;
                }
            }

            //RECHTECKSAEULE
            if (koerper == "rechtecksaeule"){
                cout << "\nSie haben die rechtecksaeule gewaehlt";

                cout << "\nWas moechten Sie berechnen?\nvolumen\noberflaeche\n";
                cout << "Geben Sie zum Auswaehlen einer Berechnung den jeweiligen Namen ein: ";
                cin >> berechnung;

                //VOLUMEN
                if (berechnung == "volumen"){
                    cout << "\nGeben Sie zuerst die kantenlaenge_a in Zentimetern ein: ";
                    cin >> kantenlaenge_a;
                    cout << "\nGeben Sie die kantenlaenge_b in Zentimetern ein: ";
                    cin >> kantenlaenge_b;
                    cout << "\nGeben Sie die kantenlaenge_c in Zentimetern ein: ";
                    cin >> kantenlaenge_c;

                    volumen = kantenlaenge_a * kantenlaenge_b * kantenlaenge_c;
                    cout << "\nDas Volumen des Koerpers betraegt: " << volumen << "cm^3";
                        return 0;
                }

                //OBERFLAECHE
                else if (berechnung == "oberflaeche"){
                    cout << "\nGeben Sie die kantenlaenge_a in Zentimetern ein: ";
                    cin >> kantenlaenge_a;
                    cout << "\nGeben Sie die kantenlaenge_b in Zentimetern ein: ";
                    cin >> kantenlaenge_b;
                    cout << "\nGeben Sie die kantenlaenge_c in Zentimetern ein: ";
                    cin >> kantenlaenge_c;

                    oberflaeche = 2 * (kantenlaenge_a * kantenlaenge_b + kantenlaenge_a * kantenlaenge_c + kantenlaenge_b * kantenlaenge_c);
                    cout << "Die Oberflaeche des Koerpers betraegt: " << oberflaeche << " cm^2";
                        return 0;

                }
                //FEHLERMELDUNG EINGABE
                else {
                    cout << "Bitte geben Sie eine korrekte Berechnungsbezeichnung ein!";
                        return 0;
                }
            }
            //KEGEL
            if (koerper == "kegel"){
                cout << "\nSie haben den kegel gewaehlt";

                cout << "\nWas moechten Sie berechnen?\nvolumen\noberflaeche\n";
                cout << "Geben Sie zum Auswaehlen einer Berechnung den jeweiligen Namen ein: ";
                cin >> berechnung;
                //VOLUMEN
                if (berechnung == "volumen"){
                    cout << "\nGeben Sie den Radius in Zentimetern an: ";
                    cin >> radius;
                    cout << "\nGeben Sie die Hoehe des Koerpers in Zentimetern an: ";
                    cin >> hoehe;
                    //rechnet hier auch 0 aus
                    volumen = M_PI * (1/3) * pow(radius,2) * hoehe;
                    cout << "Das Volumen des Koerpers betraegt: " << volumen << "cm^3";
                        return 0;

                }
                //OBERFLAECHE
                else if (berechnung == "oberflaeche"){
                    cout << "\nGeben Sie den Radius in Zentimetern an: ";
                    cin >> radius;
                    cout << "\nGeben Sie die Hoehe des Koerpers in Zentimetern an: ";
                    cin >> hoehe;

                    mantelflaeche = sqrt(hoehe * hoehe + radius * radius) * radius * M_PI;
                    cout << "\nDie Mantelflaeche betraegt: " << mantelflaeche << "cm^2";

                    oberflaeche = pow(radius,2) * M_PI + mantelflaeche;
                    cout << "\nDie Oberflaeche betraegt: " << oberflaeche << "cm^2";
                        return 0;
                }
                else {
                    cout << "Bitte geben Sie eine korrekte Berechnungsbezeichnung ein!";
                        return 0;
                }
            }
            //QU_PYRAMIDE
            if (koerper == "qu_pyramide"){
                cout << "\nSie haben die quadratische pyramide gewaehlt";

                cout << "\nWas moechten Sie berechnen?\nvolumen\noberflaeche\n";
                cout << "Geben Sie zum Auswaehlen einer Berechnung den jeweiligen Namen ein: ";
                cin >> berechnung;
                    return 0;
                //VOLUMEN
               if(berechnung == "volumen"){
                    cout << "\nGeben Sie die Kantenlaenge_a in Zentimetern ein: ";
                    cin >> kantenlaenge_a;
                    cout << "\nGeben Sie die Hoehe in Zentimetern ein: ";
                    cin >> hoehe;

                    volumen = pow(kantenlaenge_a,2) * (1/3) * hoehe;
                    cout << "\nDas Volumen des Koerpers betraegt: " << volumen << "cm^3";
                        return 0;
                }
                //OBERFLAECHE
                else if (berechnung == "oberflaeche"){
                    cout << "\nGeben Sie die Kantenlaenge_a in Zentimetern ein: ";
                    cin >> kantenlaenge_a;
                    cout << "\nGeben Sie die Hoehe in Zentimetern ein: ";
                    cin >> hoehe;
                    //spuckt hier vlt auch was falsches aus
                    mantelflaeche = kantenlaenge_a * sqrt(4 * pow(hoehe,2) + pow(kantenlaenge_a,2));
                    cout << "\nDie Mantelflaeche betraegt: " << mantelflaeche << "cm^2";

                    volumen = kantenlaenge_a * kantenlaenge_a + mantelflaeche;
                    cout << "\nDas Volumen betraegt: " << volumen << "cm^3";
                        return 0;
                }
                else {
                    cout << "Bitte geben Sie eine korrekte Berechnungsbezeichnung ein!";
                }
            }
            //ALLGEMEINE FEHLERMELDUNG EINGABE

            cout << "\nBitte geben Sie einen korrekten Namen ein!";

   /* cout << "Was moechten Sie berechnen?\nvolumen\noberflaeche\nkantenlaenge\n";
    cout << "Geben Sie zum Auswaehlen einer Berechnung den jeweiligen Namen ein: "; */
}



