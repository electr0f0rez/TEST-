# TEST
```
///---------------------------------------------------------------------------------------------------------------------------------------------------------------
//kirju­ta programm mis küsib kasutajalt tema nime ja parooli
string õigeNimi = "Danila";
string õigeParool = "12345";

Console.Writeline("Sisesta nimi: ");
string nimi = Console.ReadLine();

Console.WriteLine("Sisesta parool: ");
string parool = Console.ReadLine();

if (nimi == õigeNimi && parool == õigeParool)
{
    Console.WriteLine($"Tere tulemast, {nimi}!");
}
else
{
    Console.WriteLine("Vale nimi või parool");
}
//-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

//kirju­ta programm mis küsib kasutajalt nime (tsükli)
string nimi = "";

do
{
    Console.Write("Sisesta oma nimi: ");
    nimi = Console.ReadLine();
} while (nimi == "");

Console.WriteLine($"Tere, {nimi}");

//kirju­ta programm mis küsib kasutajalt parooli (tsükli)

string õigeParool = "12345";
string parool = "";

do
{
    Console.Write("Sisesta parool: ");
    parool = Console.ReadLine();
} while (parool != õigeParool);

Console.WriteLine("Parool on õige");

string nimi = "";

//-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

//Vanuse kontroll(IF + &&)

kirjuta programm mis küsib vanuse ja kontrollib vahemikku

Console.WriteLine("Sisesta oma vanus: ");
int vanus = int.Parse(Console.ReadLine());

if (vanus > 0 && vanus < 18)
{
    Console.WriteLine("....");
}
else if (vanus >= 18)
{
    Console.WriteLine("...");
}
else
{
    Console.WriteLine("....");
}


//-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

//Switch case näide
Console.Write("Sisesta kuu nimi: ");
string kuu = Console.ReadLine();

switch (kuu)
{
    case "detsember":
        Console.WriteLine("Talv");
        break;
    case "juuni":
        Console.WriteLine("Suvi");
        break;
    default:
        Console.WriteLine("Tundmatu kuu");
        break;
}

//-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


//Tsükkel + IF

string kasutajaNimi = "";
do
{
    Console.WriteLine("Palun sisesta oma kasutajanimi");
    kasutajaNimi = Console.ReadLine();
}
while (kasutajaNimi != "user1");

if (kasutajaNimi == "user1")
{
    int ruuduSuurus = 0;

    do
    {
        Console.WriteLine("Kui suurt ruutu tahad?");
        ruuduSuurus = int.Parse(Console.ReadLine());
    }
    while (ruuduSuurus < 0 && ruuduSuurus > 20);

    char reaKujund = '!';
    string yksRida = "";
    int tsukliMuutuja = ruuduSuurus;
    do
    {
        yksRida += "_" + reaKujund;
        tsukliMuutuja -= 1;
    } while (tsukliMuutuja != 0);
    tsukliMuutuja = ruuduSuurus;
    do
    {
        Console.WriteLine(üksRida);
        tsukliMuutuja -= 1;
    }
    while (tsukliMuutuja != 0);

    Console.WriteLine($"Palun, siin on sinu ruut, suurusega {ruuduSuurus}x{ruuduSuurus}");
}


//-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

//IF + ELSE IF + ELSE harud 
Console.WriteLine("Mis on sinu nimi?");
string nimi = Console.ReadLine();

if (nimi! == null) 
{
    Console.WriteLine("Tere " + nimi + "!");
}
else if (nimi == "")
{
    Console.WriteLine("Kasutaja ei sisestanud oma nime");
}

Console.WriteLine(nimi + ", mis on sinu vanus:");
int kasutajavanus = int.Parse(Console.ReadLine());

if (kasutajavanus < 0)
{
    Console.WriteLine("Sa ei saa olla negatiivse vanusega!");

}
else if (kasutajavanus < 16)
{
    Console.WriteLine("Kahjuks sa oled liiga noor, et osta Monsterit.");
}
else
{
    Console.WriteLine("Saad osta Monsterit!");
}

Console.WriteLine("Sisesta praegune temperatuur");
double temp = double.Parse(Console.ReadLine());

if (temp < 0)
{
    Console.WriteLine("põrgu jäätus");
}
else if (temp >= 0 && temp <= 10)
{
    Console.WriteLine("päris külm on");
}
else if (temp >= 11 && temp <= 20)
{
    Console.WriteLine("normaalne ilm");
}
else if (temp >= 21 && temp <= 30)
{
    Console.WriteLine("kas läheb grillimiseks");
}
else if (temp >= 31 && temp <= 40)
{
    Console.WriteLine("APPI; GLOBAALNE SOJENEMINE");
}


Console.WriteLine("Kas sa tahad vaarikat, maasikat või apelsini?");
string valik = Console.ReadLine();

if (valik == "vaarikat")
{
    Console.WriteLine("näe, varikas!");
}
else if (valik == "maasikat")
{
    Console.WriteLine("maasikaski on!");
}
else if (valik == "apelsini")
{
    Console.WriteLine("apelsini mul kashjuks ei ole :C");
}

//----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

//mobifix parandusautomaat (if + switch + while)
Console.WriteLine("Tere tulemust mobifix parandusautomaati! Kuidas saan aidata");
Console.WriteLine("0 - headaega\n1 - tahan telefoni parandada");
Console.WriteLine("palun tee valik, kirjutades vastav arv:");
int valik = int.Parse(Console.ReadLine());
while (valik < 0 && valik > 1)
{
    Console.WriteLine("Palun tee oma valik, kirjatades vastav arv");
    valik = int.Parse(Console.ReadLine());
}
if (valik == 0)
{
    Console.WriteLine("Headaega, tulge teinekord jälle!");
}
else
{
    Console.WriteLine("palun sisesta oma telefoni mudel, mida parandada soovid:");
    Console.WriteLine("1-iFöön\n2-xiaomjäu\n3-nihuawei\n4-Scamsung");
    Console.WriteLine("palun tee valik, kirjutades vastav arv:");
    int telefonimudel = 0;
    telefonimudel = int.Parse(Console.ReadLine());
    while (telefonimudel < 1 && telefonimudel > 4)
    {
        telefonimudel = int.Parse(Console.ReadLine());
        Console.WriteLine("palun tee valik, kirjutades vastav arv:");
    }
    switch (telefonimudel)
    {
        case 1:
            Console.WriteLine("Aitah, oma iFööni saaad tagasi 1 nädala pärast");
            break;
        case 2:
            Console.WriteLine("Aitah, sinu xiomjäu on valmis tagasi 2 kuu pärast");
            break;
        case 3:
            Console.WriteLine("Kahjuks me nihuaweid ei teneninda");
            break;
        case 4:
            Console.WriteLine("SinuScamsung on valmis 2 päeva pärast");
            break;
        default:
            Console.WriteLine("Ei tunne sellist telefonitootjat");
            break;
    }

}

//-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



//väljastada kasutaja sisestatud mängud konsooli (if - else)

namespace SõneÜlesanne1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                //kirjuta programm mis
                //küsib kasutajalt tsüklis, millised mängud talle meeldivad
                List<string> kasutajaMängud = new List<string>();

                string mängunimi = "";
                Console.WriteLine("Millised mängud sulle meeldivad?");
                while (mängunimi != "ei ole")
                {
                    Console.WriteLine("palun sisesta järgmine mäng, kui rohkem ei ole, kirjuta \"ei ole\"");
                    mängunimi = Console.ReadLine();
                    if (mängunimi != "ei ole")
                    {
                        //küsimiste tulemus hoia järjendis
                        kasutajaMängud.Add(mängunimi);
                    }



                }

                //kui järjend sisaldab (.Contains()) "mario kart", siis küsi kui vana ta on, sarkastiliselt.
                if (kasutajaMängud.Contains("mario kart"))
                {
                    Console.WriteLine("MIKS SA MARIO KARTI MÄNGID, MINGI 5 OLED VÄI?!?!");
                }

                //kui järjend sisaldab "gta 6", siis küsi kust ta ajamasina sai, et rockstar lõpuks asjaga valmis sai

                if (kasutajaMängud.Contains("gta 6"))
                {
                    Console.WriteLine("kust ta ajamasina said? kuidas rockstar sellega juba valmis sai?");
                }

                //kui järjend sisaldab "pong", siis ütle "80ndad tahavad vanureid tagasi, toimub boomerite recall"

                if (kasutajaMängud.Contains("pong"))
                {
                    Console.WriteLine("80ndad tahavad vanureid tagasi, toimub boomerite recall");
                }

                //kui järjend on tühi, siis programm läheb edasi ->

                if (kasutajaMängud.Any())
                {
                    //küsi kasutajalt kas talle ei meeldi mängud, ning löase tal vastata sõnaga jah või ei, kontrolli kasutaja sisestust .ToUpper() või .ToLower()iga
                    Console.WriteLine("KAs sulle ei meeldi mängud? vasta kas jah või ei:");
                    string jahvõiei = Console.ReadLine().ToLower();
                    //kui ta vastab jah, siis ütle, "aga miks siis ei sisestanud?"
                    if (jahvõiei.Contains("jah"))
                    {
                        Console.WriteLine("aga miks siis ei sisestanud?");
                    }
                    //kui talle ei meeldi, siis ütle, kahju
                    else if (jahvõiei.Contains("ei"))
                    {
                        Console.WriteLine("kahju :c");
                    }
                    //kui vastus on midagi muud, siis ütle "ei saa aru :/".
                    else
                    {
                        Console.WriteLine("ei saa aru :/");
                    }
                }
            }
        }
    }

//-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

//Muuda konsooli taustavärvi kasutaja lemmikvärvi järgi (if + else if + else)
Console.WriteLine("Milline värv sulle kõige rohkem meeldib?:");
    string favouriteColour = Console.ReadLine();
            if (favouriteColour == "punane")

            {
                Console.BackgroundColor = ConsoleColor.Red;
            }
if (favouriteColour == "oranz")
{
    Console.WriteLine("Kahjuks oranzi ei ole");
}
if (favouriteColour == "roheline")
{
    Console.BackgroundColor = ConsoleColor.Green;
}
else
{
    Console.WriteLine("Värvi ei tunne");
}
Console.WriteLine("Värv suudetud!");


//-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

//Ostukorv (metoodika + tsükkel + tingimuslause)
internal class Program
{
    private static void Main(string[] args)
    {
        NewMessage();
        List<string> ostunimekiri = new List<string>();
        Console.WriteLine("sisesta oma tänane poeskäigunimekiri");
        string kasutajaSisestus = "";
        GetUserInput(kasutajaSisestus, ostunimekiri);
        foreach (var söök in ostunimekiri)
        {
            Console.WriteLine($" -*- {söök}");
        }
        GetUserInput(kasutajaSisestus, ostunimekiri);

    }

    static List<string> GetUserInput(string kasutajasisestus, List<string> ostunimekiri)
    {
        while (kasutajasisestus != "rohkem pole")
        {
            Console.WriteLine("Kirjuta ükshaaval, sisesta järgmine ost:\nKui rohkem ei ole midagi lisada, siis ütle \"rohkem pole\""); ;
            kasutajasisestus = Console.ReadLine();
            if (kasutajasisestus != "" || kasutajasisestus != "rohkem pole")
            {
                ostunimekiri.Add(kasutajasisestus);
            }
            else if (kasutajasisestus == "rohkem pole")
            {
                kasutajasisestus = "";
            }
        }
        Console.WriteLine("See sinu nimekiri");
        return ostunimekiri;
    }

    static void NewMessage()
    {
        Console.WriteLine("this is a message");
    }
}

//-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

//Muuda konsooli taustavärvi kasutaja lemmikvärvide järgi (switch + tsükkel + list)
Console.WriteLine("MIs on su lemmikvärvid? Sisesta palun ükshaaval\nKui rohkem värve ei ole, kirjuta \"rohkem pole\"");
List<string> kasutajaVärvid = new List<string>();

string sisestus = "";
do
{
    Console.WriteLine("Sisesta 1 värv korraga: ");
    sisestus = Console.ReadLine();

    if (sisestus != "rohkem pole")
    {
        kasutajaVärvid.Add(sisestus);
    }

} while (sisestus != "rohkem pole");

foreach (var värv in kasutajaVärvid)
{
    switch (värv)
    {
        // punane, oranz, kollane, roheline, helesinine, tumeroheline, lilla,
        // roosa, pruun, must, valge, hall, värvi-ei-tunta
        // roosa & oranz - neid värve ei ole, tagasta sõnum mis on värevispetsiifiline
        case "punane":
            Console.BackgroundColor = ConsoleColor.Red;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- p u n a n e -*-*-");
            break;
        /* LISAGE ISESEISVALT KÕIKIDE MUUDE VÄRVIDE CASED */
        case "oranz":
            Console.BackgroundColor = ConsoleColor.Black;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("Oranz pole saadaval");
            break;
        case "kollane":
            Console.BackgroundColor = ConsoleColor.Yellow;
            Console.ForegroundColor = ConsoleColor.Black;
            Console.WriteLine("-*-*- k o l l a n e -*-*-");
            break;
        case "roheline":
            Console.BackgroundColor = ConsoleColor.Green;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- r o h e l i n e -*-*-");
            break;
        case "helesinine":
            Console.BackgroundColor = ConsoleColor.DarkBlue;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- h e l e s i n i n e -*-*-");
            break;
        case "tumeroheline":
            Console.BackgroundColor = ConsoleColor.DarkGreen;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- t u m e r o h e l i n e -*-*-");
            break;
        case "lilla":
            Console.BackgroundColor = ConsoleColor.Magenta;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- p u n a n e -*-*-");
            break;
        case "pruun":
            Console.BackgroundColor = ConsoleColor.DarkYellow;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- p r u u n ? -*-*-");
            break;
        case "must":
            Console.BackgroundColor = ConsoleColor.Black;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine("-*-*- m u s t -*-*-");
            break;

        default:
            Console.BackgroundColor = ConsoleColor.Black;
            Console.ForegroundColor = ConsoleColor.White;
            Console.WriteLine($"Ei tunne sellist värvi{värv}");
            break;

    }
}



//-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------




//Kasutaja autentimine + lemmikloomade nimekiri (if + while + massiiv)
{
    // -- 1: küsime nime ja parooli
    string correctName = "Danila";
        string correctPassword = "12345";

        Console.Write("Sisesta oma nimi: ");
        string userName = Console.ReadLine();

        // kontrollime, kas nimi on õige
        if (userName != correctName)
        {
            Console.WriteLine($"Isik {userName} ei ole registreeritud!");
            return;
        }

        Console.Write("Sisesta oma parool:");
        string userPassword = Console.ReadLine();

        // kontrollime, kas parool on õige
        if (userPassword != correctPassword)
        {
            Console.WriteLine($"Vale parool, {userName}!");
            return;
        }

        // -- 2: mõlemad õiged ---
        Console.WriteLine($"Tere tulemast, {userName}!");

        // loome massiivi suurusega 3
        string[] pets = new string[3];
        int count = 0;

        // -- 3: while-tsükkel lemmikloomade jaoks 
        while (count < pets.Length)
        {
            Console.Write($"Sisesta lemmiklooma nimi {count + 1}: (kui lemmiklomomad kõik kirjatasid sis kirjuda 'kõik'");
            string pet = Console.ReadLine();

            if (string.IsNullOrWhiteSpace(pet))
            {
                Console.WriteLine("Nimi ei tohi olla tühi!");
                continue;
            }
            pets[count] = pet;
            count++;
        }

        // -- 4: näitame mitu nime sisestati 
        Console.WriteLine($"Sa sisestasid {count} lemmiklooma nime.");

        // kuvame kõik sisestatud nimed
        Console.WriteLine("Sinu lemmikloomad on:");
        for (int i = 0; i < pets.Length; i++)
        {
            Console.WriteLine($"{i + 1}. {pets[i]}");
        }

        // -- 5: küsime, milline on lemmikloom
        Console.WriteLine("Milline neist on su kõige lemmikum? (sisesta number 1-3):");
        string valik = Console.ReadLine();
        int index = int.Parse(valik);
        string favorite = pets[index];
        index = index + 1;



        // kuvame tulemuse
        Console.WriteLine(userName + ", sinu kõige lemmikloom on " + favorite);
    }
}

//-----------------------------------------
namespace MinuKonspekt
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine(/*abc*/"hapukapsas");
            // "Console"   -> on moodul C# mida me adresserime, Console aitab teha tegevusi käsureal
            //             -> näitab, et meil on vaja adresseerida mingisugust funktsiooni või meetodit mooduli "Console" seest.
            // "WriteLine" -> Funktsioon mida me parasjagu kasutame.
            // ()          -> sulupaar mis omab funktsiooni tööks vajalikku infot
            // []          -> tähistab massiive
            // {}          -> koodiplokk, tavaliselt kas pärast (if, else if) tingimust, namespace'i või funktsiooni kirjeldust
            // "hapukapsas"-> parameeter mis antakse funktsioonile WriteLine töötlemiseks kaasa.
            //              //    -> Taane aitab arendajal aru saada, kuskohas millise koodiploki sees kood asub, see on vajalik ka kompilaatorile samal eesmärgil.
            //             -> kõik koodilause lõppevad komakooloniga, mis tähistavad lause lõppu
            //             -> tähistab üherealist kommentaari
            // /**/        -> tähistab mitmerealist kommentaari või kommentaariregiooni

            int muutuja = 3;
            // int         -> on muutuja nime ees olev andmetüübi kirjaldus mis näitab ära, millist
            //                tüüpi andmed selle muutuja sees on.
            // "muutuja"   -> on nimetus, ehk muutuja, mis noiab endas mingeid sndmeid, inimloetava
            //                sõnaga, ja mille abil saab neid addresseerida koodi sees.
            // =           -> üksik võrdsmärk omistab muutuja sisse vastava vääruse mis asub 
            //                teiselpool võrdusmärki.
            // 3           -> muutujale omistatav väärtus.

            /* Võimalikud andmetüübid mida vaja võib minna: */
            int a = 1; // int on täisarv
            decimal b = 2.1M; // desimal on kümnendsüsteemis olev komakohaga arv
            float c = 3.9f; //float on 32-biitine komakohaga arv
            double d = 5.6d; // double on 64-bitine komakohaga arv
            char cl = 'a'; // üksainus täht või tähemark mis asub ülakomadde vahel 
            string s = "tekst"; //tähtedest koosnev sõna või tekast, tähistatakse jutmärkidega ""
            var X = "abc"; //var on ebamäärase andmetüübiga kohalik muutuja 
            var y = 123;   //ta võib omada endas teisi andmetüüpi
            const int z = 9; // konstant-tüüpi muutujaid ei saa muuta, nende sise on read-only

            //põhilised matemaatilised tehted
            int liitimne = 1 + 1; //liitmine, kaks arvu liidetakse kokku
            int lahutamine = 1 - 1; //lahutamine, kus esimesest arvust lahutatakse maha teine
            double korrutamine = 1 * 2; //korrutamine, kus teine arv korrutatakse esimise arvu kordi.
            double jagamine = 1 / 2; //jagamine. esimine arv jagatakse teise arvuga.
            double astendamine = Math.Pow(2, 2); //astendamine, esimine arv astendatakse teisega
double juurimine = Math.Sqrt(2); //ruutjuur, parameetrina juuritav arv

            //muutuja nimed 
            int arv = 0;
            string sõne = "abc";
            //string string = "abc"; //kaitsud sõna kasutada ei saa

            // muutuja nimeks ei sobi järgnevad sõnad:
            //abstract, as, base, bool, break, byte, case
            //catch, char, cheched, class, count, continue, decimal,
            //default, delegate, do, double, else, enum, event,
            //explicit, extern, false, finally, fixed, float, for
            //foreach, goto, if, implicit, in, int, interface, internal
            //is, lock, long, namespace, new, null, object, operator,
            //out, override, params, private, protected, public, readonly,
            //ref, return, sbyte, sealed, short, sizeof, stackalloc,
            //static, string, struct, switch, this, throw, try, typeof, uint
            //uint, ulong, unchecked, unsafe, ushort, using, virtual,
            //void, volatile, while.



            //3 kalkulaator ifi ja elsifidega
            Console.WriteLine("Tere. Sisesta esimene arv");
            // Adresserime moodulit "Console", punkti abil ütleme, et kasutame funktsiooni WriteLine 
            // selle jaoks et öelda kasutajale sõnum mis asub funktsiooni nime järel sulgude vahel 
            // ümbritsetuna jutumärkidega. Kasutajale esitatav sõnum on "Tere. Sisesta esimene arv".

            int arv1 = int.Parse(Console.ReadLine());
            //instantsieerime muutuja nimega "arvl", ning selle ette anname andmetüübiks"int", see 
            //ütleb ära, et siin muutujas on täisarvud sees. Omistame muutujale võrdusmärgi abil 
            //väärtuse, mille saame kasutajalt. Selle jaoks, adresseerime uuesti "Console" moodulit 
            //Aga seekord on funktsiooni nimi "ReadLine". Selleks, et käsureapealt tulev arv programmile 
            //tekstina ei näe välja, küsime int mooduli seest omakorda funktsiooni "Parse", ning paneme
            //ReadLine funktsiooni Parse() sulgude vahele.


            Console.WriteLine("Tere. Sisesta teine arv");


            int arv2 = int.Parse(Console.ReadLine());
            Console.WriteLine("Sisesta tehtmärk: / * + -");
            //Adresseerime moodulit "Console" koos "WriteLine" funktsiooniga, et esitada kasutajale 
            //küsimuse "Sisesta tehtemärk: / * + -". Punkti abil saame moodulist Console, funktsiooni 
            //WriteLine, ning sulgude vahel ongi kasutajale esitatav tekst. Tekst ise on ka ümbritsetud
            //jutumärkidega. Lause lõppeb lauselõpumärgiga ";".



            string tehtetyyp = Console.ReadLine();
            //instantsieerime muutuja nimega "tehtetyyp", mille ette kirjutame andmetüübiks "string".
            //Omistame võrdusmärgi abil, sellesse muutujasse kasutajalt sisendi mille saame kasutade.
            //"Console" moodulis oleva ReadLine() funktsiooni abil. Lause lõppeb lauselõpumärgiga ";".


            int tulemus = 0;
            //instantsieerime muutuja nimega "tulemus", andmetüübiga int, ning omistame talle algse 
            //väärtuse võrdusmärgi abil, milleks on 0. Lause lõppeb lauselõpumärgiga ";".


            if (tehtetyyp == "+")
            //teeme tingimuslause if, ning selle tingimuse määrame ära sulgudega,mille vahel on
            //võrdsuskontroll. Kontrollime kas muutuja "tehtetyyp" omab andmeid samalkujul 
            //nagu võrdusmärkidest teisel pool olev tekst "+". Siin lause ei lõppe, kuna tegu ei
            //ole koodiga mis midagi kindlalt veel ära teeb.


            {
                tulemus = arv1 + arv2;
            }
            //peale tingimust on koodiplokk {} sulgude vahel, mis sialdab endas ühte koodirida.
            //selles lauses omistame muutujale "tulemus" võrdusmärgi abil liitmistehte tulemuse,
            //kus liidame kokku muutuja "arv1" ja muutuja "arv2" sisu. Lause lõppeb lauselõpumärgiga ";".


            else if (tehtetyyp == "-")
            //teeme sekundaarse tingimuslause "else if", ning määrame tema tingimuse ära sulgudega.
            //Sulgude vahel on võrdsuskontroll. Kontrollime kas muutuja "tehtetyyp" omab andmeid
            //samal kujul nagu võrdusmärkidest teisel pool olev tekst "-" kui eelnev tingimus ei
            //täitunud. Lause siin ei lõppe, vaid tingimusele järgneb koodiplokk.

            {
                tulemus = arv1 - arv2;
            }
            //peale tingimust on koodiplokk {} loogeliste sulgude vahel, mis sisaldab endas ühte
            //koodirida. selles lauses omistame muutujale "tulemus" võrdusmärgi abil lahutustehte
            //tulemuse, kus lahutame muutuja "arv" sees olevast väärtusest maha "arv2" muutujas
            //oleva väärtuse. Lause lõppeb lauselõpumärgiga ",".

            else if (tehtetyyp == "/")
            //teeme sekundaarse tingimuslause "else if", ning määrassme tema tingimuse ära sulgudega. 
            //Sulgude vahel on võrdsuskontroll. Kontrollime kas muutuja "tehtetyyp" omab andmeid
            //samal kujul nagu võrdusmärkidest teisel pool olev tekst "/" kui eelnev tingimus eʻi
            //täitunud. Lause siin ei lõppe, vaid tingimusele järgneb koodiplokk.
            {
                tulemus = arv1 / arv2;
            }
            //peale tingimust on koodiplokk {} loogeliste sulgude vahel, mis sisaldabendas ühte 
            //koodirida. selles lauses omistame muutujale "tulemus" võrdusmärgi abil korrutustehte 
            //tulemuse, kus korrutame muutujas "arv2" oleva väärtuse, muutujas "arv1" oleva väärtuse
            //kordi. Lause lõppeb lauselõpumärgiga ";".

            else if (tehtetyyp == "*")
            //teeme sekundaarse tingimuslause "else if", ning määrame tema tingimuse ära sulgudega.
            //Sulgude vahel on võrdsuskontroll. Kontrollime kas muutuja "tehtetyyp" omab andmeid
            //samal kujul nagu võrdusmärkidest teisel pool olev tekst "*" kui eelnev tingimus ei
            //täitunud. Lause siin ei lõppe, vaid tingimusele järgneb koodiplokk.
            {
                tulemus = arv1 * arv2;
            }
            //peale tingimust on koodiplokk {} loogeliste sulgude vahel, mis sisaldab endas ühte 
            //koodirida. selles lauses omistame muutujale "tulemus" võrdusmärgi abil korrutustehte 
            //tulemuse, kus korrutame muutujas "arv2" oleva väärtuse muutujas "arv1" oleva väärtuse
            //kordi. Lause lõppeb lauselõpumärgiga ";".

            else if (tehtetyyp == "^")
            //teeme sekundaarse tingimuslause "else if", ning määrame tema tingimuse ära sulgudega.
            //Sulgude vahel on võrdsuskontroll, kontrollime kas muutuja "tehtetyyp" omab andmeid 
            //samal kujul nagu võrdusmärkidest teisel pool olev tekst "^" kui eelnev tingimus ei
            //täitunud. Lause siin ei lõppe, vaid tingimusele järgneb koodiplokk.
            {
                tulemus = (int)Math.Pow(arv1, arv2);
            }
            //peale tingimust on koodiplokk {} loogeliste sulgude vahel, mis sisaldab endas ühte 
            //koodirida. Selles lauses omistatakse võrdusmärgi abil muutujasse "tulemus" mille saame 
            //"Math" moodulist pärineva funktsiooni "Pow()" abil. Math Pow() võtab parameetritena
            //sisse muutjad "arv1" ja "arv2". Esimene parameeter on astendatav, teine parameeter 
            //on astendaja. Funktsiooni Math.Pow() ees on kiirteisendus (int), kuna muutuja 
            //"tulemus" andmetüüp on täisarv. Math Pow() väljund teisendatakse nii täisarvuks.
            //Lause lõppeb lauselöpumärgiga ";".


            else
            //peale kõiki järeltingimusi on meil tingimuslause osa "else" mida täidetakse kõikide 
            //muude tingimuslause osade mittetäitumisel. Siin eraldi tingimust välja ei kirjutada 
            //ning sellest tulenevalt ei ole ka sulge. Järgneb ainult koodiplokk.
            {
                Console.WriteLine("Palun sisesta tehe, mida kalkulaator tavustada oskab");
            }
            //peale "else" on koodiplokk {} loogeliste sulgude vahel, mis sisaldab endas ühte 
            //koodirida. Selles koodireas kasutame moodulist "Console" punkti abil funktsiooni 
            //"WriteLine" et öelda kasutajale "Palun sisesta tehe, mida kalkulaator tuvastada
            //oskab". Koodirida lõppeb lauselõpumärgiga ";".


            Console.WriteLine(tulemus);
            //Kasutame moodulist "Console" punkti abil funktsiooni "WriteLine" et kuvada kasutajale 
            //tehte tulemus. Selle jaoks on WriteLine funktsioonis parameetrina pandud muutuja
            //"tulemus" ilma tekstiks teisendamata. Lause lõppeb lauselõpumärgiga ";".

        }
    }
}







Tools → Options → Text Editor → C# → IntelliSense
IntelliCode
Advanced - Responsive code completion
