#include <stdio.h>
#include <string.h>

#define MAX_MOVIES 10

typedef struct {
    char title[50];
    char language[20];
    char genre[20];
    int year;
} Movie;

/*  Array with 10 movies for each (language, genre) */
Movie movies[] = {

    /* ENGLISH – SCI-FI  */
    {"Inception",              "English", "Sci-Fi",   2010},
    {"Interstellar",           "English", "Sci-Fi",   2014},
    {"The Matrix",             "English", "Sci-Fi",   1999},
    {"Avatar",                 "English", "Sci-Fi",   2009},
    {"The Martian",            "English", "Sci-Fi",   2015},
    {"Blade Runner 2049",      "English", "Sci-Fi",   2017},
    {"Arrival",                "English", "Sci-Fi",   2016},
    {"Edge of Tomorrow",       "English", "Sci-Fi",   2014},
    {"Jurassic Park",          "English", "Sci-Fi",   1993},
    {"Star Wars: A New Hope",  "English", "Sci-Fi",   1977},

    /* English -Comedy*/
    {"American Pie",           "English", "Comedy",   1999},
    {"We're the Millers",           "English", "Comedy",  2013},
    {"The Hangover",           "English", "Comedy",   2009},
    {"Superbad",           "English", "Comedy",   2007},
    {"Eurotrip",           "English", "Comedy",   2004},
    {"Roadtrip",           "English", "Comedy",   2000},
    {"The Girl Next Door",           "English", "Comedy",   2004},
    {"21 Jump street",           "English", "Comedy",   2012},
    {"American Pie",           "English", "Comedy",   1999},
    {"Blended",           "English", "Comedy",   2014},


    /* ENGLISH – ACTION  */
    {"The Dark Knight",        "English", "Action",   2008},
    {"Mad Max: Fury Road",     "English", "Action",   2015},
    {"Gladiator",              "English", "Action",   2000},
    {"John Wick",              "English", "Action",   2014},
    {"Avengers: Endgame",      "English", "Action",   2019},
    {"Die Hard",               "English", "Action",   1988},
    {"The Avengers",           "English", "Action",   2012},
    {"Mission: Impossible - Fallout","English","Action",2018},
    {"Terminator 2: Judgment Day","English","Action", 1991},
    {"The Bourne Ultimatum",   "English", "Action",   2007},

    /* ENGLISH – ROMANCE  */
    {"Titanic",                "English", "Romance",  1997},
    {"La La Land",             "English", "Romance",  2016},
    {"The Notebook",           "English", "Romance",  2004},
    {"Pride and Prejudice",    "English", "Romance",  2005},
    {"A Star Is Born",         "English", "Romance",  2018},
    {"Notting Hill",           "English", "Romance",  1999},
    {"Me Before You",          "English", "Romance",  2016},
    {"Crazy Rich Asians",      "English", "Romance",  2018},
    {"500 Days of Summer",     "English", "Romance",  2009},
    {"The Fault in Our Stars", "English", "Romance",  2014},

    /* ENGLISH – CRIME  */
    {"The Godfather",          "English", "Crime",    1972},
    {"The Godfather Part II",  "English", "Crime",    1974},
    {"Pulp Fiction",           "English", "Crime",    1994},
    {"The Departed",           "English", "Crime",    2006},
    {"Se7en",                  "English", "Crime",    1995},
    {"Goodfellas",             "English", "Crime",    1990},
    {"The Irishman",           "English", "Crime",    2019},
    {"Heat",                   "English", "Crime",    1995},
    {"Reservoir Dogs",         "English", "Crime",    1992},
    {"The Usual Suspects",     "English", "Crime",    1995},

    /* ENGLISH – DRAMA  */
    {"Forrest Gump",           "English", "Drama",    1994},
    {"The Shawshank Redemption","English","Drama",    1994},
    {"Fight Club",             "English", "Drama",    1999},
    {"The Pursuit of Happyness","English","Drama",    2006},
    {"The Green Mile",         "English", "Drama",    1999},
    {"A Beautiful Mind",       "English", "Drama",    2001},
    {"The Social Network",     "English", "Drama",    2010},
    {"Whiplash",               "English", "Drama",    2014},
    {"Birdman",                "English", "Drama",    2014},
    {"Million Dollar Baby",    "English", "Drama",    2004},

    /* ENGLISH – THRILLER  */
    {"Inception",              "English", "Thriller", 2010},
    {"Shutter Island",         "English", "Thriller", 2010},
    {"Gone Girl",              "English", "Thriller", 2014},
    {"The Silence of the Lambs","English","Thriller", 1991},
    {"The Prestige",           "English", "Thriller", 2006},
    {"Memento",                "English", "Thriller", 2000},
    {"Prisoners",              "English", "Thriller", 2013},
    {"Zodiac",                 "English", "Thriller", 2007},
    {"Black Swan",             "English", "Thriller", 2010},
    {"Nightcrawler",           "English", "Thriller", 2014},

    /* HINDI – -Comedy(10)*/
    {"3 Idiots",               "Hindi",   "Comedy",   2009},
    {"Andaz Apna Apna",       "Hindi",   "Comedy",   1994},
    {"Hera Pheri",             "Hindi",   "Comedy",   2000},
    {"Chupke Chupke",          "Hindi",   "Comedy",   1975},
    {"Munna Bhai M.B.B.S.",    "Hindi",   "Comedy",   2003},
    {"Welcome",                "Hindi",   "Comedy",   2007},
    {"Bhool Bhulaiyaa",        "Hindi",   "Comedy",   2007},
    {"Golmaal: Fun Unlimited", "Hindi",   "Comedy",   2006},
    {"Dhamaal",                "Hindi",   "Comedy",   2007},
    {"Pyaar Ka Punchnama",     "Hindi",   "Comedy",   2011},



    /* HINDI – ACTION (10) */
    {"Sholay",              "Hindi", "Action", 1975},
{"Dabangg",             "Hindi", "Action", 2010},
{"Singham",             "Hindi", "Action", 2011},
{"War",                 "Hindi", "Action", 2019},
{"Ghajini",             "Hindi", "Action", 2008},
{"Dhoom",               "Hindi", "Action", 2004},
{"Dhoom 2",             "Hindi", "Action", 2006},
{"Ek Tha Tiger",        "Hindi", "Action", 2012},
{"Baaghi",              "Hindi", "Action", 2016},
{"Wanted",              "Hindi", "Action", 2009},


    /* HINDI – DRAMA (10) */
     {"Dangal",               "Hindi", "Drama", 2016},
{"Taare Zameen Par",    "Hindi", "Drama", 2007},
{"Lagaan",              "Hindi", "Drama", 2001},
{"Swades",              "Hindi", "Drama", 2004},
{"Bajrangi Bhaijaan",   "Hindi", "Drama", 2015},
{"Gangs of Wasseypur",  "Hindi", "Drama", 2012},
{"My Name Is Khan",     "Hindi", "Drama", 2010},
{"Pink",                "Hindi", "Drama", 2016},
{"Masaan",              "Hindi", "Drama", 2015},
{"Barfi!",              "Hindi", "Drama", 2012},



    /* HINDI – ROMANCE (10) */
    {"Dilwale Dulhania Le Jayenge", "Hindi", "Romance", 1995},
{"Kuch Kuch Hota Hai",          "Hindi", "Romance", 1998},
{"Kal Ho Naa Ho",               "Hindi", "Romance", 2003},
{"Jab We Met",                  "Hindi", "Romance", 2007},
{"Veer-Zaara",                  "Hindi", "Romance", 2004},
{"Yeh Jawaani Hai Deewani",     "Hindi", "Romance", 2013},
{"Aashiqui 2",                  "Hindi", "Romance", 2013},
{"Kabir Singh",                 "Hindi", "Romance", 2019},
{"Hum Tum",                     "Hindi", "Romance", 2004},
{"Rockstar",                    "Hindi", "Romance", 2011},


    /* HINDI – THRILLER (10) */
    {"Drishyam",            "Hindi", "Thriller", 2015},
{"Kahaani",             "Hindi", "Thriller", 2012},
{"A Wednesday!",        "Hindi", "Thriller", 2008},
{"Talaash",             "Hindi", "Thriller", 2012},
{"Special 26",          "Hindi", "Thriller", 2013},
{"Andhadhun",          "Hindi", "Thriller", 2018},
{"Badla",               "Hindi", "Thriller", 2019},
{"Talvar",              "Hindi", "Thriller", 2015},
{"Ugly",                "Hindi", "Thriller", 2013},
{"Karthik Calling Karthik", "Hindi", "Thriller", 2010},


    /* HINDI – SCI-FI (10) */
    {"Koi... Mil Gaya",      "Hindi", "Sci-Fi", 2003},
{"Krrish",               "Hindi", "Sci-Fi", 2006},
{"Krrish 3",             "Hindi", "Sci-Fi", 2013},
{"Ra.One",               "Hindi", "Sci-Fi", 2011},
{"Robot 2.0 (Hindi)",    "Hindi", "Sci-Fi", 2018},
{"PK",                   "Hindi", "Sci-Fi", 2014},
{"Mr. India",            "Hindi", "Sci-Fi", 1987},
{"Attack",               "Hindi", "Sci-Fi", 2022},
{"A Flying Jatt",        "Hindi", "Sci-Fi", 2016},
{"Joker",                "Hindi", "Sci-Fi", 2012},



    /* KANNADA – ACTION (10) */
{"K.G.F: Chapter 1",  "Kannada", "Action", 2018},
{"K.G.F: Chapter 2",  "Kannada", "Action", 2022},
{"Ugramm",            "Kannada", "Action", 2014},
{"Vikrant Rona",      "Kannada", "Action", 2022},
{"The Villain",       "Kannada", "Action", 2018},
{"Avane Srimannarayana","Kannada","Action",2019},
{"Upendra",           "Kannada", "Action", 1999},
{"Uppi 2",            "Kannada", "Action", 2015},
{"Raktha Kanneeru",   "Kannada", "Action", 2003},
{"Kenda",             "Kannada", "Action", 2024},

/* KANNADA – DRAMA (10) */
{"Thithi",            "Kannada", "Drama", 2015},
{"Sarkari Hi. Pra. Shaale, Kasaragodu, Koduge: Ramanna Rai","Kannada","Drama",2018},
{"Kantara",           "Kannada", "Drama", 2022},
{"Garuda Gamana Vrishabha Vahana","Kannada","Drama",2021},
{"777 Charlie",       "Kannada", "Drama", 2022},
{"Gantumoote",        "Kannada", "Drama", 2019},
{"Kannadiga",         "Kannada", "Drama", 2021},
{"Kavirathna Kaalidaasa","Kannada","Drama",1983},
{"As Seen by the Rest","Kannada","Drama",2014},
{"Thurthu Nirgamana", "Kannada", "Drama", 2022},

/* KANNADA – ROMANCE (10) */
{"Mungaru Male",      "Kannada", "Romance", 2006},
{"Kirik Party",       "Kannada", "Romance", 2016},
{"Dia",               "Kannada", "Romance", 2020},
{"Love Mocktail",     "Kannada", "Romance", 2020},
{"Ek Love Ya",        "Kannada", "Romance", 2022},
{"Chamak",            "Kannada", "Romance", 2017},
{"Ondu Motteya Kathe","Kannada", "Romance", 2017},
{"Rathnan Prapancha", "Kannada", "Romance", 2021},
{"777 Charlie",       "Kannada", "Romance", 2022},
{"Mungaru Male 2",    "Kannada", "Romance", 2016},

/* KANNADA – COMEDY (10) */
{"Kirik Party",       "Kannada", "Comedy", 2016},
{"Ondu Motteya Kathe","Kannada", "Comedy", 2017},
{"Chamak",            "Kannada", "Comedy", 2017},
{"Avane Srimannarayana","Kannada","Comedy",2019},
{"777 Charlie",       "Kannada", "Comedy", 2022},
{"Govinda Govinda",   "Kannada", "Comedy", 2021},
{"Bell Bottom",       "Kannada", "Comedy", 2019},
{"Love Mocktail",     "Kannada", "Comedy", 2020},
{"Rathnan Prapancha", "Kannada", "Comedy", 2021},
{"Mayabazar 2016",    "Kannada", "Comedy", 2016},

/* KANNADA – THRILLER (10) */
{"Lucia",             "Kannada", "Thriller", 2013},
{"RangiTaranga",      "Kannada", "Thriller", 2015},
{"Kavalu Daari",      "Kannada", "Thriller", 2019},
{"Ugramm",            "Kannada", "Thriller", 2014},
{"K.G.F: Chapter 1",  "Kannada", "Thriller", 2018},
{"K.G.F: Chapter 2",  "Kannada", "Thriller", 2022},
{"Vikrant Rona",      "Kannada", "Thriller", 2022},
{"Thurthu Nirgamana", "Kannada", "Thriller", 2022},
{"Garuda Gamana Vrishabha Vahana","Kannada","Thriller",2021},
{"U Turn",            "Kannada", "Thriller", 2016},

/* KANNADA – SCI-FI (10) */
{"Lucia",             "Kannada", "Sci-Fi", 2013},
{"Tora Tora",         "Kannada", "Sci-Fi", 2017},
{"Blink",             "Kannada", "Sci-Fi", 2024},
{"Consilium",         "Kannada", "Sci-Fi", 2022},
{"Mandala: The UFO Incident","Kannada","Sci-Fi",2023},
{"Gana",              "Kannada", "Sci-Fi", 2024},
{"Kaadumale",         "Kannada", "Sci-Fi", 2025},
{"Kaadu Male",        "Kannada", "Sci-Fi", 2025},
{"Kanna Muchhe Kaade Goode","Kannada","Sci-Fi",2024},
{"Shalivahana Shakhe","Kannada", "Sci-Fi", 2024},


    /* TELUGU – ACTION (10) */
{"Baahubali: The Beginning",  "Telugu", "Action", 2015},
{"Baahubali 2: The Conclusion","Telugu","Action", 2017},
{"RRR",                       "Telugu", "Action", 2022},
{"Pushpa: The Rise",          "Telugu", "Action", 2021},
{"Magadheera",                "Telugu", "Action", 2009},
{"Akhanda",                   "Telugu", "Action", 2021},
{"Sarileru Neekevvaru",       "Telugu", "Action", 2020},
{"Sye Raa Narasimha Reddy",   "Telugu", "Action", 2019},
{"Aravinda Sametha Veera Raghava","Telugu","Action",2018},
{"Major",                     "Telugu", "Action", 2022},

/* TELUGU – DRAMA (10) */
{"Mahanati",                  "Telugu", "Drama", 2018},
{"Jersey",                    "Telugu", "Drama", 2019},
{"Srimanthudu",               "Telugu", "Drama", 2015},
{"Ala Vaikunthapurramuloo",   "Telugu", "Drama", 2020},
{"Naandhi",                   "Telugu", "Drama", 2021},
{"C/o Kancharapalem",         "Telugu", "Drama", 2018},
{"Middle Class Melodies",     "Telugu", "Drama", 2020},
{"Brochevarevarura",          "Telugu", "Drama", 2019},
{"Kanche",                    "Telugu", "Drama", 2015},
{"Vedam",                     "Telugu", "Drama", 2010},

/* TELUGU – ROMANCE (10) */
{"Arjun Reddy",               "Telugu", "Romance", 2017},
{"Geetha Govindam",           "Telugu", "Romance", 2018},
{"Fidaa",                     "Telugu", "Romance", 2017},
{"Ye Maya Chesave",           "Telugu", "Romance", 2010},
{"Ninnu Kori",                "Telugu", "Romance", 2017},
{"Tholi Prema",               "Telugu", "Romance", 1998},
{"Ala Modalaindi",            "Telugu", "Romance", 2011},
{"Bommarillu",                "Telugu", "Romance", 2006},
{"Premam",                    "Telugu", "Romance", 2016},
{"100% Love",                 "Telugu", "Romance", 2011},

/* TELUGU – COMEDY (10) */
{"Ashta Chamma",              "Telugu", "Comedy", 2008},
{"Jathi Ratnalu",             "Telugu", "Comedy", 2021},
{"F2: Fun and Frustration",   "Telugu", "Comedy", 2019},
{"Venky",                     "Telugu", "Comedy", 2004},
{"Dhee",                      "Telugu", "Comedy", 2007},
{"Oohalu Gusagusalade",       "Telugu", "Comedy", 2014},
{"Bhale Bhale Magadivoy",     "Telugu", "Comedy", 2015},
{"Eedo Rakam Aado Rakam",     "Telugu", "Comedy", 2016},
{"Ami Thumi",                 "Telugu", "Comedy", 2017},
{"Nenu Local",                "Telugu", "Comedy", 2017},

/* TELUGU – THRILLER (10) */
{"Eega",                      "Telugu", "Thriller", 2012},
{"Goodachari",                "Telugu", "Thriller", 2018},
{"Kshanam",                   "Telugu", "Thriller", 2016},
{"1: Nenokkadine",            "Telugu", "Thriller", 2014},
{"Anukokunda Oka Roju",       "Telugu", "Thriller", 2005},
{"Agent Sai Srinivasa Athreya","Telugu","Thriller", 2019},
{"Aithe",                     "Telugu", "Thriller", 2003},
{"Karthikeya",                "Telugu", "Thriller", 2014},
{"Run Raja Run",              "Telugu", "Thriller", 2014},
{"Hit: The First Case",       "Telugu", "Thriller", 2020},

/* TELUGU – SCI-FI (10) */
{"Aditya 369",                "Telugu", "Sci-Fi",   1991},
{"Jagadeka Veerudu Athiloka Sundari","Telugu","Sci-Fi",1990},
{"Eega",                      "Telugu", "Sci-Fi",   2012},
{"Baahubali: The Beginning",  "Telugu", "Sci-Fi",   2015},
{"Baahubali 2: The Conclusion","Telugu","Sci-Fi",   2017},
{"Agnyaathavaasi",            "Telugu", "Sci-Fi",   2018},
{"Okka Kshanam",              "Telugu", "Sci-Fi",   2017},
{"24",                        "Telugu", "Sci-Fi",   2016},
{"Yashoda",                   "Telugu", "Sci-Fi",   2022},
{"Hanu-Man",                  "Telugu", "Sci-Fi",   2024},


    /* TAMIL – ACTION (10) */
{"Baashha",              "Tamil", "Action", 1995},
{"Kaakha Kaakha",        "Tamil", "Action", 2003},
{"Thuppakki",            "Tamil", "Action", 2012},
{"Vikram",               "Tamil", "Action", 2022},
{"Thani Oruvan",         "Tamil", "Action", 2015},
{"Madras",               "Tamil", "Action", 2014},
{"Aaranya Kaandam",      "Tamil", "Action", 2010},
{"Vada Chennai",         "Tamil", "Action", 2018},
{"Kaithi",               "Tamil", "Action", 2019},
{"Maanaadu",             "Tamil", "Action", 2021},

/* TAMIL – DRAMA (10) */
{"Nayagan",              "Tamil", "Drama", 1987},
{"Anbe Sivam",           "Tamil", "Drama", 2003},
{"Pithamagan",           "Tamil", "Drama", 2003},
{"Deiva Thirumagal",     "Tamil", "Drama", 2011},
{"Bombay",               "Tamil", "Drama", 1995},
{"Moondram Pirai",       "Tamil", "Drama", 1982},
{"Rhythm",               "Tamil", "Drama", 2000},
{"Vaanathaippola",       "Tamil", "Drama", 2000},
{"Mozhi",                "Tamil", "Drama", 2007},
{"Karnan",               "Tamil", "Drama", 2021},

/* TAMIL – ROMANCE (10) */
{"Alaipayuthey",         "Tamil", "Romance", 2000},
{"Vinnaithaandi Varuvaayaa","Tamil","Romance", 2010},
{"Roja",                 "Tamil", "Romance", 1992},
{"Mouna Ragam",          "Tamil", "Romance", 1986},
{"Kadhal",               "Tamil", "Romance", 2004},
{"Minnale",              "Tamil", "Romance", 2001},
{"'96",                  "Tamil", "Romance", 2018},
{"O Kadhal Kanmani",     "Tamil", "Romance", 2015},
{"Raja Rani",            "Tamil", "Romance", 2013},
{"Oh My Kadavule",       "Tamil", "Romance", 2020},

/* TAMIL – COMEDY (10) */
{"Thillu Mullu",         "Tamil", "Comedy", 1981},
{"Boss Engira Bhaskaran","Tamil", "Comedy", 2010},
{"Siva Manasula Sakthi", "Tamil", "Comedy", 2009},
{"Kalakalappu",          "Tamil", "Comedy", 2012},
{"Soodhu Kavvum",        "Tamil", "Comedy", 2013},
{"Maanagaram",           "Tamil", "Comedy", 2017},
{"Velaiyilla Pattathari", "Tamil","Comedy", 2014},
{"Varuthapadatha Valibar Sangam","Tamil","Comedy",2013},
{"Kanaa Kandaen",        "Tamil", "Comedy", 2005},
{"Anniyan" ,             "Tamil", "Comedy", 2005},  // action‑thriller with strong comic track

/* TAMIL – THRILLER (10) */
{"Jigarthanda",          "Tamil", "Thriller", 2014},
{"Pudhupettai",          "Tamil", "Thriller", 2006},
{"Aaranya Kaandam",      "Tamil", "Thriller", 2010},
{"Vishwaroopam",         "Tamil", "Thriller", 2013},
{"Maanagaram",           "Tamil", "Thriller", 2017},
{"Ratsasan",             "Tamil", "Thriller", 2018},
{"Game Over",            "Tamil", "Thriller", 2019},
{"Vikram Vedha",         "Tamil", "Thriller", 2017},
{"Dhuruvangal Pathinaaru","Tamil","Thriller", 2016},
{"Thani Oruvan",         "Tamil", "Thriller", 2015},

/* TAMIL – SCI-FI (10) */
{"Enthiran",             "Tamil", "Sci-Fi", 2010},
{"2.0",                  "Tamil", "Sci-Fi", 2018},
{"Indru Netru Naalai",   "Tamil", "Sci-Fi", 2015},
{"24",                   "Tamil", "Sci-Fi", 2016},
{"Irandam Ulagam",       "Tamil", "Sci-Fi", 2013},
{"Mayavan",              "Tamil", "Sci-Fi", 2017},
{"Tamiluku En Ondrai Aluthavum","Tamil","Sci-Fi",2015},
{"Maanaadu",             "Tamil", "Sci-Fi", 2021},
{"Mudhalvan",            "Tamil", "Sci-Fi", 1999},   // political sci‑fi angle
{"Kalai Arasi",          "Tamil", "Sci-Fi", 1963}

};

int totalMovies = sizeof(movies) / sizeof(movies[0]);

void showLanguageMenu() {
    printf("\n====== LANGUAGE MENU ======\n");
    printf("1. English\n");
    printf("2. Hindi\n");
    printf("3. Kannada\n");
    printf("4. Telugu\n");
    printf("5. Tamil\n");
    printf("6. Exit\n");
    printf("Enter language choice (1-6): ");
}

void showGenreMenu() {
    printf("\n------ GENRE MENU ------\n");
    printf("1. Action\n");
    printf("2. Comedy\n");
    printf("3. Drama\n");
    printf("4. Romance\n");
    printf("5. Thriller\n");
    printf("6. Sci-Fi\n");
    printf("Enter genre choice (1-6): ");
}

void getLanguageName(int choice, char *language) {
    switch (choice) {
        case 1: strcpy(language, "English"); break;
        case 2: strcpy(language, "Hindi");   break;
        case 3: strcpy(language, "Kannada"); break;
        case 4: strcpy(language, "Telugu");  break;
        case 5: strcpy(language, "Tamil");   break;
        default: language[0] = '\0';
    }
}

void getGenreName(int choice, char *genre) {
    switch (choice) {
        case 1: strcpy(genre, "Action");  break;
        case 2: strcpy(genre, "Comedy");  break;
        case 3: strcpy(genre, "Drama");   break;
        case 4: strcpy(genre, "Romance"); break;
        case 5: strcpy(genre, "Thriller");break;
        case 6: strcpy(genre, "Sci-Fi");  break;
        default: genre[0] = '\0';
    }
}

void showMovies(const char *language, const char *genre, int minYear, int maxYear) {
    int count = 0;
    printf("\nTop %d %s movies in %s between %d and %d:\n",
           MAX_MOVIES, genre, language, minYear, maxYear);
    printf("----------------------------------------\n");
    for (int i = 0; i < totalMovies && count < MAX_MOVIES; i++) {
        if (strcmp(movies[i].language, language) == 0 &&
            strcmp(movies[i].genre, genre) == 0 &&
            movies[i].year >= minYear &&
            movies[i].year <= maxYear) {
            printf("%d. %s (%d)\n", count + 1, movies[i].title, movies[i].year);
            count++;
        }
    }
    if (count == 0) {
        printf("No movies found for this combination and year range.\n");
    }
    printf("----------------------------------------\n");
}


int main() {
    int langChoice, genreChoice;
    int minYear, maxYear;
    char language[20], genre[20];

    while (1) {
        showLanguageMenu();
        if (scanf("%d", &langChoice) != 1) break;

        if (langChoice == 6) {
            printf("Exiting Movie Recommendation System. Goodbye!\n");
            break;
        }

        getLanguageName(langChoice, language);
        if (language[0] == '\0') {
            printf("Invalid language choice. Try again.\n");
            continue;
        }

        showGenreMenu();
        if (scanf("%d", &genreChoice) != 1) break;

        getGenreName(genreChoice, genre);
        if (genre[0] == '\0') {
            printf("Invalid genre choice. Try again.\n");
            continue;
        }

        printf("Enter minimum year: ");
        scanf("%d", &minYear);
        printf("Enter maximum year: ");
        scanf("%d", &maxYear);

        showMovies(language, genre, minYear, maxYear);
    }

    return 0;
}
