<template>
  <div id="nav">
  </div>
  <router-view>
    <div class="test-grid">
      <CustomGrid
        :data="data"
        :columns="columns"
        @clickedRow="(row) => log(row)"
      />
    </div>
  </router-view>
</template>

<script setup>
import { ref } from "@vue/reactivity";
import CustomGrid from '@/components/Grid/CustomGrid.vue'
let data = ref([{
  "first_name": "Harri",
  "last_name": "Bidnall",
  "gender": "Female",
  "email": "hbidnall0@1688.com",
  "password": "WJ6o4Oh5",
  "App": "Lotstring",
  "car_model": 2003,
  "city": "Kunčina",
  "domain": "sciencedirect.com",
  "movie": "Drama",
  "pet": "Blackbuck",
  "buzz_word": "installation"
}, {
  "first_name": "Dorry",
  "last_name": "Schowenburg",
  "gender": "Female",
  "email": "dschowenburg1@mail.ru",
  "password": "xMVGJraO",
  "App": "Matsoft",
  "car_model": 2011,
  "city": "Allanridge",
  "domain": "youku.com",
  "movie": "Drama|War",
  "pet": "Bottle-nose dolphin",
  "buzz_word": "Organized"
}, {
  "first_name": "Mathilda",
  "last_name": "Flemyng",
  "gender": "Genderfluid",
  "email": "mflemyng2@mac.com",
  "password": "vokMwsx",
  "App": "Konklux",
  "car_model": 2007,
  "city": "Kongolo",
  "domain": "cyberchimps.com",
  "movie": "Drama|Fantasy|Sci-Fi",
  "pet": "Common palm civet",
  "buzz_word": "mission-critical"
}, {
  "first_name": "Zebedee",
  "last_name": "Sollon",
  "gender": "Male",
  "email": "zsollon3@addthis.com",
  "password": "UKWN3kWL",
  "App": "Matsoft",
  "car_model": 1992,
  "city": "Blagaj",
  "domain": "histats.com",
  "movie": "Comedy|Horror",
  "pet": "Madagascar fruit bat",
  "buzz_word": "Exclusive"
}, {
  "first_name": "Camilla",
  "last_name": "Mort",
  "gender": "Female",
  "email": "cmort4@guardian.co.uk",
  "password": "dfAG6mrKHLk",
  "App": "Flexidy",
  "car_model": 1987,
  "city": "Conde",
  "domain": "vimeo.com",
  "movie": "Drama",
  "pet": "Wallaroo, common",
  "buzz_word": "Universal"
}, {
  "first_name": "Lynett",
  "last_name": "Gladdish",
  "gender": "Female",
  "email": "lgladdish5@google.it",
  "password": "EWPTcRbqaQ",
  "App": "Aerified",
  "car_model": 2010,
  "city": "Staré Město",
  "domain": "altervista.org",
  "movie": "Comedy",
  "pet": "Laughing dove",
  "buzz_word": "Multi-layered"
}, {
  "first_name": "Gwynne",
  "last_name": "Oxenham",
  "gender": "Female",
  "email": "goxenham6@tmall.com",
  "password": "S5wW0K",
  "App": "Stim",
  "car_model": 2006,
  "city": "Sekararum",
  "domain": "woothemes.com",
  "movie": "Action|Thriller",
  "pet": "Cat, miner's",
  "buzz_word": "Persistent"
}, {
  "first_name": "Addy",
  "last_name": "Oxburgh",
  "gender": "Male",
  "email": "aoxburgh7@prlog.org",
  "password": "mlLpKrvWDv",
  "App": "Otcom",
  "car_model": 2010,
  "city": "Kunwi",
  "domain": "google.pl",
  "movie": "Drama",
  "pet": "Dunnart, fat-tailed",
  "buzz_word": "Seamless"
}, {
  "first_name": "Virgie",
  "last_name": "Keitch",
  "gender": "Male",
  "email": "vkeitch8@csmonitor.com",
  "password": "JvNcVMTVg",
  "App": "Matsoft",
  "car_model": 2007,
  "city": "Tinabogan",
  "domain": "fema.gov",
  "movie": "Drama",
  "pet": "Porcupine, north american",
  "buzz_word": "Synergistic"
}, {
  "first_name": "Cherie",
  "last_name": "Jumel",
  "gender": "Female",
  "email": "cjumel9@aboutads.info",
  "password": "SGSMH1Vc",
  "App": "Bigtax",
  "car_model": 1993,
  "city": "Austin",
  "domain": "homestead.com",
  "movie": "Drama",
  "pet": "Porcupine, tree",
  "buzz_word": "Team-oriented"
}, {
  "first_name": "Hermann",
  "last_name": "Alway",
  "gender": "Male",
  "email": "halwaya@netscape.com",
  "password": "2Itix5ZeipC",
  "App": "Span",
  "car_model": 1993,
  "city": "Seara",
  "domain": "si.edu",
  "movie": "Comedy|Crime|Mystery",
  "pet": "Tiger cat",
  "buzz_word": "transitional"
}, {
  "first_name": "Diena",
  "last_name": "Pigrome",
  "gender": "Genderfluid",
  "email": "dpigromeb@infoseek.co.jp",
  "password": "a18AEyCwf",
  "App": "Alpha",
  "car_model": 1999,
  "city": "Ponta Grossa",
  "domain": "columbia.edu",
  "movie": "Action|Drama",
  "pet": "Lilac-breasted roller",
  "buzz_word": "collaboration"
}, {
  "first_name": "Julita",
  "last_name": "Hynd",
  "gender": "Female",
  "email": "jhyndc@bluehost.com",
  "password": "iD7u9jm8",
  "App": "Ventosanzap",
  "car_model": 1988,
  "city": "Čajetina",
  "domain": "yelp.com",
  "movie": "Drama|Horror|Thriller",
  "pet": "Deer, red",
  "buzz_word": "Integrated"
}, {
  "first_name": "Jabez",
  "last_name": "McDunlevy",
  "gender": "Male",
  "email": "jmcdunlevyd@irs.gov",
  "password": "mDhc0MDWuO",
  "App": "Temp",
  "car_model": 1991,
  "city": "Nginokrajan",
  "domain": "sphinn.com",
  "movie": "Drama",
  "pet": "Collared lemming",
  "buzz_word": "bottom-line"
}, {
  "first_name": "Dorisa",
  "last_name": "Hayward",
  "gender": "Female",
  "email": "dhaywarde@soup.io",
  "password": "XlvWSqPp",
  "App": "Namfix",
  "car_model": 1998,
  "city": "Rawuk",
  "domain": "ask.com",
  "movie": "Drama|Horror|Romance",
  "pet": "Francolin, swainson's",
  "buzz_word": "Organized"
}, {
  "first_name": "Emogene",
  "last_name": "Desseine",
  "gender": "Agender",
  "email": "edesseinef@mashable.com",
  "password": "kq6u8ImJ7YtV",
  "App": "Stronghold",
  "car_model": 2008,
  "city": "Pingsha",
  "domain": "phpbb.com",
  "movie": "Comedy|Documentary",
  "pet": "Saddle-billed stork",
  "buzz_word": "archive"
}, {
  "first_name": "Alan",
  "last_name": "Thebe",
  "gender": "Bigender",
  "email": "athebeg@hc360.com",
  "password": "89j5Bz7F",
  "App": "Zontrax",
  "car_model": 2000,
  "city": "Masons Bay",
  "domain": "wp.com",
  "movie": "Action|Adventure|Thriller",
  "pet": "Coatimundi, white-nosed",
  "buzz_word": "Self-enabling"
}, {
  "first_name": "Tanhya",
  "last_name": "Edlyn",
  "gender": "Female",
  "email": "tedlynh@webnode.com",
  "password": "5ghYuGwjEp5",
  "App": "Hatity",
  "car_model": 2001,
  "city": "Akhmīm",
  "domain": "lycos.com",
  "movie": "Action|Drama|War",
  "pet": "Leopard, indian",
  "buzz_word": "Centralized"
}, {
  "first_name": "Amby",
  "last_name": "Cloney",
  "gender": "Male",
  "email": "acloneyi@earthlink.net",
  "password": "6x3S4F4pdt",
  "App": "Wrapsafe",
  "car_model": 2003,
  "city": "Heka",
  "domain": "zimbio.com",
  "movie": "Drama|Romance|War",
  "pet": "Hornbill, southern ground",
  "buzz_word": "Synchronised"
}, {
  "first_name": "Felike",
  "last_name": "Burnsall",
  "gender": "Male",
  "email": "fburnsallj@shop-pro.jp",
  "password": "gPpsOAKIf",
  "App": "Veribet",
  "car_model": 2009,
  "city": "Miasskoye",
  "domain": "w3.org",
  "movie": "Action|Comedy|Crime|Thriller",
  "pet": "Caiman, spectacled",
  "buzz_word": "architecture"
}, {
  "first_name": "Kristo",
  "last_name": "Curtois",
  "gender": "Male",
  "email": "kcurtoisk@thetimes.co.uk",
  "password": "zyEznSXxs",
  "App": "Latlux",
  "car_model": 2008,
  "city": "Ruse",
  "domain": "mac.com",
  "movie": "Drama|Romance",
  "pet": "Crowned eagle",
  "buzz_word": "upward-trending"
}, {
  "first_name": "Etheline",
  "last_name": "Bothe",
  "gender": "Female",
  "email": "ebothel@slashdot.org",
  "password": "18kFh1hgT3s",
  "App": "Bamity",
  "car_model": 2009,
  "city": "Sirre",
  "domain": "weather.com",
  "movie": "Drama|Romance|Western",
  "pet": "Sungazer, yellow-brown",
  "buzz_word": "hub"
}, {
  "first_name": "Kat",
  "last_name": "Joye",
  "gender": "Female",
  "email": "kjoyem@archive.org",
  "password": "4lDXcSx5t3",
  "App": "Zathin",
  "car_model": 2002,
  "city": "Illapel",
  "domain": "sitemeter.com",
  "movie": "Drama",
  "pet": "Nelson ground squirrel",
  "buzz_word": "Fundamental"
}, {
  "first_name": "Munroe",
  "last_name": "Hovel",
  "gender": "Male",
  "email": "mhoveln@histats.com",
  "password": "FUO9ORty991d",
  "App": "Tempsoft",
  "car_model": 2005,
  "city": "Ljubno ob Savinji",
  "domain": "yelp.com",
  "movie": "Comedy|Romance",
  "pet": "Three-banded plover",
  "buzz_word": "zero defect"
}, {
  "first_name": "Daren",
  "last_name": "Cardero",
  "gender": "Male",
  "email": "dcarderoo@cmu.edu",
  "password": "4xP7qZsOvkO",
  "App": "Zaam-Dox",
  "car_model": 2000,
  "city": "Kampen (Overijssel)",
  "domain": "wix.com",
  "movie": "Drama",
  "pet": "Oriental white-backed vulture",
  "buzz_word": "bi-directional"
}, {
  "first_name": "Beaufort",
  "last_name": "Muxworthy",
  "gender": "Male",
  "email": "bmuxworthyp@yahoo.co.jp",
  "password": "xWqySOg",
  "App": "Opela",
  "car_model": 2005,
  "city": "Temaiku Village",
  "domain": "yellowbook.com",
  "movie": "Crime|Drama|Thriller",
  "pet": "White-fronted bee-eater",
  "buzz_word": "Team-oriented"
}, {
  "first_name": "Joana",
  "last_name": "Cawthera",
  "gender": "Female",
  "email": "jcawtheraq@people.com.cn",
  "password": "Q2icygp6KIV",
  "App": "Tresom",
  "car_model": 1994,
  "city": "Dzerzhinskiy",
  "domain": "nba.com",
  "movie": "Documentary",
  "pet": "Snow goose",
  "buzz_word": "Multi-tiered"
}, {
  "first_name": "Lewie",
  "last_name": "Esche",
  "gender": "Male",
  "email": "lescher@cam.ac.uk",
  "password": "IJQpFNylDtIZ",
  "App": "Bytecard",
  "car_model": 1983,
  "city": "Liangli",
  "domain": "earthlink.net",
  "movie": "Comedy",
  "pet": "Yellow baboon",
  "buzz_word": "intranet"
}, {
  "first_name": "Lelah",
  "last_name": "Merriton",
  "gender": "Female",
  "email": "lmerritons@bing.com",
  "password": "aosIE3PEkdAK",
  "App": "Redhold",
  "car_model": 1990,
  "city": "Drobin",
  "domain": "indiatimes.com",
  "movie": "Comedy|Drama",
  "pet": "Woylie",
  "buzz_word": "national"
}, {
  "first_name": "Kristal",
  "last_name": "Rapper",
  "gender": "Female",
  "email": "krappert@army.mil",
  "password": "Rqkues",
  "App": "Pannier",
  "car_model": 1999,
  "city": "Cilentung",
  "domain": "altervista.org",
  "movie": "Comedy|Drama",
  "pet": "Blue fox",
  "buzz_word": "Integrated"
}, {
  "first_name": "Reinhard",
  "last_name": "Hendricks",
  "gender": "Genderfluid",
  "email": "rhendricksu@techcrunch.com",
  "password": "mroTr38fp5N",
  "App": "Subin",
  "car_model": 2004,
  "city": "Idhnā",
  "domain": "nhs.uk",
  "movie": "Comedy|Sci-Fi|Thriller",
  "pet": "Long-crested hawk eagle",
  "buzz_word": "Vision-oriented"
}, {
  "first_name": "Chad",
  "last_name": "Ramshay",
  "gender": "Male",
  "email": "cramshayv@ocn.ne.jp",
  "password": "7igBSq1I",
  "App": "Opela",
  "car_model": 1972,
  "city": "Lazurne",
  "domain": "sciencedirect.com",
  "movie": "Comedy|Drama",
  "pet": "Frilled dragon",
  "buzz_word": "approach"
}, {
  "first_name": "Therine",
  "last_name": "Turn",
  "gender": "Female",
  "email": "tturnw@vinaora.com",
  "password": "TPqlyKslhF",
  "App": "Ventosanzap",
  "car_model": 1994,
  "city": "Chowṉêy",
  "domain": "wufoo.com",
  "movie": "Drama",
  "pet": "Egyptian vulture",
  "buzz_word": "artificial intelligence"
}, {
  "first_name": "Beaufort",
  "last_name": "Casbourne",
  "gender": "Male",
  "email": "bcasbournex@ameblo.jp",
  "password": "PBLDovDhc",
  "App": "Transcof",
  "car_model": 2003,
  "city": "Shihuajian",
  "domain": "themeforest.net",
  "movie": "Drama|Romance",
  "pet": "Small-spotted genet",
  "buzz_word": "Exclusive"
}, {
  "first_name": "Dewain",
  "last_name": "Monkhouse",
  "gender": "Non-binary",
  "email": "dmonkhousey@bloglovin.com",
  "password": "xXDQeCMfL",
  "App": "Subin",
  "car_model": 1993,
  "city": "Bohicon",
  "domain": "dagondesign.com",
  "movie": "Documentary",
  "pet": "Sage hen",
  "buzz_word": "Advanced"
}, {
  "first_name": "Valdemar",
  "last_name": "True",
  "gender": "Male",
  "email": "vtruez@va.gov",
  "password": "pa7Vr7z6Zp",
  "App": "Fixflex",
  "car_model": 1995,
  "city": "Perpignan",
  "domain": "shop-pro.jp",
  "movie": "Drama",
  "pet": "Puma, south american",
  "buzz_word": "internet solution"
}, {
  "first_name": "Pamela",
  "last_name": "Joliffe",
  "gender": "Female",
  "email": "pjoliffe10@jigsy.com",
  "password": "yQ9r8GdzW",
  "App": "Fintone",
  "car_model": 2004,
  "city": "Liwan",
  "domain": "weather.com",
  "movie": "Drama|Horror|Mystery",
  "pet": "African pied wagtail",
  "buzz_word": "optimizing"
}, {
  "first_name": "Audrie",
  "last_name": "Gowthorpe",
  "gender": "Female",
  "email": "agowthorpe11@unicef.org",
  "password": "ErIYdPd",
  "App": "Holdlamis",
  "car_model": 2002,
  "city": "Březová nad Svitavou",
  "domain": "house.gov",
  "movie": "Comedy|Crime|Drama",
  "pet": "Brown and yellow marshbird",
  "buzz_word": "Extended"
}, {
  "first_name": "Judas",
  "last_name": "Zimmermanns",
  "gender": "Male",
  "email": "jzimmermanns12@statcounter.com",
  "password": "ioFrPjHh",
  "App": "Fix San",
  "car_model": 1960,
  "city": "Chengyue",
  "domain": "home.pl",
  "movie": "Drama",
  "pet": "Snake-necked turtle",
  "buzz_word": "Integrated"
}, {
  "first_name": "Ilyse",
  "last_name": "Pahler",
  "gender": "Female",
  "email": "ipahler13@ca.gov",
  "password": "kPTE8tleD",
  "App": "Daltfresh",
  "car_model": 1960,
  "city": "Lidköping",
  "domain": "slate.com",
  "movie": "Comedy",
  "pet": "Red-breasted cockatoo",
  "buzz_word": "User-friendly"
}, {
  "first_name": "Jayson",
  "last_name": "Brace",
  "gender": "Male",
  "email": "jbrace14@taobao.com",
  "password": "XqmrWB",
  "App": "Zaam-Dox",
  "car_model": 2009,
  "city": "Matagalpa",
  "domain": "51.la",
  "movie": "Action|Adventure|Fantasy|Horror",
  "pet": "Spotted wood sandpiper",
  "buzz_word": "systematic"
}, {
  "first_name": "Gery",
  "last_name": "Skoyles",
  "gender": "Male",
  "email": "gskoyles15@dell.com",
  "password": "6EmJ0W3",
  "App": "Bigtax",
  "car_model": 1986,
  "city": "Zlatograd",
  "domain": "vkontakte.ru",
  "movie": "Comedy|Documentary",
  "pet": "Skua, long-tailed",
  "buzz_word": "reciprocal"
}, {
  "first_name": "Uri",
  "last_name": "Millichip",
  "gender": "Male",
  "email": "umillichip16@reuters.com",
  "password": "XiZbBhk",
  "App": "Y-Solowarm",
  "car_model": 1989,
  "city": "Ljungby",
  "domain": "businesswire.com",
  "movie": "Comedy|Romance",
  "pet": "Black kite",
  "buzz_word": "Open-architected"
}, {
  "first_name": "Inglebert",
  "last_name": "Meyer",
  "gender": "Male",
  "email": "imeyer17@time.com",
  "password": "3Ps1gC",
  "App": "Temp",
  "car_model": 2007,
  "city": "Bogdanovich",
  "domain": "hhs.gov",
  "movie": "Comedy|Musical",
  "pet": "Steller's sea lion",
  "buzz_word": "challenge"
}, {
  "first_name": "Ellsworth",
  "last_name": "Shanahan",
  "gender": "Male",
  "email": "eshanahan18@cnn.com",
  "password": "aUiD1eEVZocc",
  "App": "Bigtax",
  "car_model": 2008,
  "city": "Likiep",
  "domain": "yahoo.com",
  "movie": "Drama",
  "pet": "Wildebeest, blue",
  "buzz_word": "Fully-configurable"
}, {
  "first_name": "Maribel",
  "last_name": "Sheerin",
  "gender": "Female",
  "email": "msheerin19@tiny.cc",
  "password": "xKoyweqEI6JG",
  "App": "Voyatouch",
  "car_model": 2008,
  "city": "Hŭngju-dong",
  "domain": "marketwatch.com",
  "movie": "Drama",
  "pet": "Sloth, two-toed tree",
  "buzz_word": "Object-based"
}, {
  "first_name": "Loise",
  "last_name": "Royan",
  "gender": "Female",
  "email": "lroyan1a@fastcompany.com",
  "password": "kNmC0xMp6",
  "App": "Andalax",
  "car_model": 1991,
  "city": "Yeniköy",
  "domain": "census.gov",
  "movie": "Documentary|War",
  "pet": "Fox, north american red",
  "buzz_word": "multi-tasking"
}, {
  "first_name": "Anson",
  "last_name": "Trowel",
  "gender": "Male",
  "email": "atrowel1b@deliciousdays.com",
  "password": "hpY4gx8Hh1R",
  "App": "Zamit",
  "car_model": 1976,
  "city": "Burnaby",
  "domain": "jimdo.com",
  "movie": "Comedy",
  "pet": "Mouse, four-striped grass",
  "buzz_word": "service-desk"
}, {
  "first_name": "Livia",
  "last_name": "Oxley",
  "gender": "Female",
  "email": "loxley1c@shutterfly.com",
  "password": "McFvpa9u5",
  "App": "Greenlam",
  "car_model": 1994,
  "city": "Pavia",
  "domain": "google.fr",
  "movie": "Drama",
  "pet": "Palm squirrel",
  "buzz_word": "impactful"
}, {
  "first_name": "Carma",
  "last_name": "Dormand",
  "gender": "Bigender",
  "email": "cdormand1d@blogspot.com",
  "password": "CAksFOW",
  "App": "Fix San",
  "car_model": 1988,
  "city": "Kipen’",
  "domain": "icq.com",
  "movie": "Comedy|Drama",
  "pet": "Silver-backed jackal",
  "buzz_word": "product"
}])
 const dataColumns = (arr) => {
    let keys = Object.keys(arr.value[0])
    let columns = []
    keys?.forEach(el => {
      let colObj = {
        title: el.toUpperCase(),
        identifier: el,
      }
      columns.push(colObj)
    })
    return columns
  }
  const columns = dataColumns(data)
  const log = (arg) => {
    console.log(arg)
  }
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.test-grid{
  margin: auto;
  width: calc(100% - 18.75rem);
  height: 50rem;
  overflow: auto;
  display: grid;
  place-items: center;
}
</style>
