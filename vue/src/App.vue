<template>
  <h1 class="Center">-CraZi Music-</h1>
  <hr />
  <SocialBox></SocialBox>

  <hr />
  <section>
    <MusicList
      @toParent="MusicDataFromChild"
      v-bind:Musics="ListofMusic"
      v-bind:Lists="ListofAdded"
    ></MusicList>
    <PlayList
      @removes="RemovedMusicData"
      v-bind:AddedMusic="ListofAdded"
    ></PlayList>
  </section>
</template>

<script>
import { gsap } from "gsap";

import SocialBox from "./components/SocialBox.vue";
import MusicList from "./components/MusicList.vue";
import PlayList from "./components/PlayList.vue";

export default {
  data() {
    return {
      ListofMusic: gsap.utils.shuffle([
        {
          year: 1994,
          artist: "Notorious B.I.G.",
          genre: "Hip hop",
          name: "Juicy",
        },
        {
          year: 1992,
          artist: "Dr. Dre",
          genre: "Gangsta rap",
          name: "Nuthin' But a G Thang",
        },

        {
          year: 1987,
          artist: "Eric B. & Rakim",
          genre: "East Coast hip hop",
          name: "Paid in Full",
        },
        {
          year: 2015,
          artist: "Kendrick Lamar",
          genre: "Hip hop",
          name: "Alright",
        },
        {
          year: 1994,
          artist: "Nas",
          genre: "Hip hop",
          name: "NY State of Mind",
        },
        {
          year: 1998,
          artist: "Lauryn Hill",
          genre: "Hip hop",
          name: "Doo Wop (That Thing)",
        },
        {
          year: 1999,
          artist: "Eminem",
          genre: "Hip hop",
          name: "My Name Is",
        },
        {
          year: 1992,
          artist: "Ice Cube",
          genre: "Gangsta rap",
          name: "It Was a Good Day",
        },
        {
          year: 1995,
          artist: "Tupac",
          genre: "Gangsta rap",
          name: "Dear Mama",
        },
        {
          year: 2004,
          artist: "Kanye West",
          genre: "Hip hop",
          name: "Jesus Walks",
        },
        {
          year: 2016,
          artist: "Chance The Rapper",
          genre: "Hip hop",
          name: "No Problem",
        },
        {
          year: 1989,
          artist: "Beastie Boys",
          genre: "Hip hop",
          name: "Paul Revere",
        },
        {
          year: 1983,
          artist: "Eiichi Ohtaki",
          genre: "City Pop",
          name: "Kimi wa Tennen Shoku",
        },
        {
          year: 1991,
          artist: "Zard",
          genre: "J-Pop",
          name: "Makenaide",
        },

        {
          year: 2018,
          artist: "Hikaru Utada feat. Skrillex",
          genre: "J-Pop",
          name: "Face My Fears",
        },
        {
          year: 2019,
          artist: "Official HIGE DANdism",
          genre: "J-Pop",
          name: "Pretender",
        },
        {
          year: 2020,
          artist: "Yonezu Kenshi",
          genre: "J-Pop",
          name: "Kanden",
        },
        {
          year: 2021,
          artist: "LiSA",
          genre: "J-Pop",
          name: "Homura",
        },
        {
          year: 1983,
          artist: "Teresa Teng",
          genre: "Mandopop",
          name: "The Moon Represents My Heart",
        },
        {
          year: 1979,
          artist: "Fei Yu-ching",
          genre: "Mandopop",
          name: "A Spray of Plum Blossoms",
        },
        {
          year: 1995,
          artist: "Jacky Cheung",
          genre: "Cantopop",
          name: "Love is Eternal",
        },
        {
          year: 2005,
          artist: "Jay Chou",
          genre: "Mandopop",
          name: "Nunchucks",
        },
        {
          year: 1992,
          artist: "Sandy Lam",
          genre: "Cantopop",
          name: "At Least I Still Have You",
        },
        {
          year: 2006,
          artist: "Eason Chan",
          genre: "Cantopop",
          name: "Time Flies",
        },
        {
          year: 1991,
          artist: "Leslie Cheung",
          genre: "Cantopop",
          name: "A Better Tomorrow",
        },
        {
          year: 1997,
          artist: "Tanya Chua",
          genre: "Mandopop",
          name: "Moonlight",
        },
        {
          year: 1983,
          artist: "Liu Wen Zheng",
          genre: "Mandopop",
          name: "What is Love",
        },
        {
          year: 1994,
          artist: "Mayday",
          genre: "Mandopop",
          name: "Contented",
        },
        {
          year: 1988,
          artist: "Sam Hui",
          genre: "Cantopop",
          name: "Days of Being Wild",
        },
        {
          year: 1989,
          artist: "Alan Tam",
          genre: "Cantopop",
          name: "Friends",
        },
        {
          year: 2014,
          artist: "Jolin Tsai",
          genre: "Mandopop",
          name: "Play",
        },
        {
          year: 2009,
          artist: "Wang Leehom",
          genre: "Mandopop",
          name,
        },
        {
          year: 1995,
          artist: "Seo Taiji and Boys",
          genre: "K-pop",
          name: "I Know",
        },
        {
          year: 2008,
          artist: "Girls' Generation",
          genre: "K-pop",
          name: "Gee",
        },
        {
          year: 2012,
          artist: "Psy",
          genre: "K-pop",
          name: "Gangnam Style",
        },
        {
          year: 2013,
          artist: "IU",
          genre: "K-pop",
          name: "Good Day",
        },
        {
          year: 2011,
          artist: "Big Bang",
          genre: "K-pop",
          name: "Fantastic Baby",
        },
        {
          year: 2010,
          artist: "2NE1",
          genre: "K-pop",
          name: "I Am The Best",
        },
        {
          year: 1998,
          artist: "g.o.d",
          genre: "K-pop",
          name: "To Mother",
        },
        {
          year: 2010,
          artist: "Super Junior",
          genre: "K-pop",
          name: "Bonamana",
        },
        {
          year: 2016,
          artist: "BTS",
          genre: "K-pop",
          name: "Blood Sweat & Tears",
        },
        {
          year: 2009,
          artist: "2PM",
          genre: "K-pop",
          name: "Heartbeat",
        },
        {
          year: 2010,
          artist: "CNBLUE",
          genre: "K-pop",
          name: "I'm a Loner",
        },
        {
          year: 2015,
          artist: "Red Velvet",
          genre: "K-pop",
          name: "Dumb Dumb",
        },
        {
          year: 2014,
          artist: "EXO",
          genre: "K-pop",
          name: "Overdose",
        },
        {
          year: 2003,
          artist: "Rain",
          genre: "K-pop",
          name: "It's Raining",
        },
        {
          year: 2011,
          artist: "f(x)",
          genre: "K-pop",
          name: "Electric Shock",
        },
        {
          year: 2011,
          artist: "T-ara",
          genre: "K-pop",
          name: "Roly Poly",
        },
        {
          year: 2007,
          artist: "Wonder Girls",
          genre: "K-pop",
          name: "Tell Me",
        },
        {
          year: 2014,
          artist: "Akdong Musician",
          genre: "K-pop",
          name: "200%",
        },
        {
          year: 2001,
          artist: "BoA",
          genre: "K-pop",
          name: "Atlantis Princess",
        },
        {
          year: 2004,
          artist: "TVXQ",
          genre: "K-pop",
          name: "Hug",
        },
        {
          year: 1984,
          artist: "Prince",
          genre: "Pop/Rock",
          name: "Purple Rain",
        },
        {
          year: 1965,
          artist: "The Beatles",
          genre: "Rock",
          name: "Yesterday",
        },
        {
          year: 1971,
          artist: "John Lennon",
          genre: "Rock",
          name: "Imagine",
        },
        {
          year: 1977,
          artist: "Fleetwood Mac",
          genre: "Pop/Rock",
          name: "Dreams",
        },
        {
          year: 1994,
          artist: "TLC",
          genre: "R&B",
          name: "Waterfalls",
        },
        {
          year: 1983,
          artist: "Michael Jackson",
          genre: "Pop/Rock",
          name: "Billie Jean",
        },
        {
          year: 1991,
          artist: "Nirvana",
          genre: "Rock",
          name: "Smells Like Teen Spirit",
        },
        {
          year: 1968,
          artist: "The Rolling Stones",
          genre: "Rock",
          name: "Sympathy for the Devil",
        },
        {
          year: 1977,
          artist: "David Bowie",
          genre: "Pop/Rock",
          name: "Heroes",
        },
        {
          year: 1977,
          artist: "Queen",
          genre: "Rock",
          name: "We Will Rock You",
        },
        {
          year: 1977,
          artist: "Sex Pistols",
          genre: "Punk Rock",
          name: "God Save the Queen",
        },
        {
          year: 1989,
          artist: "Madonna",
          genre: "Pop",
          name: "Like a Prayer",
        },
        {
          year: 1999,
          artist: "Eminem",
          genre: "Hip-Hop",
          name: "My Name Is",
        },
        {
          year: 1991,
          artist: "Metallica",
          genre: "Metal",
          name: "Enter Sandman",
        },
        {
          year: 1995,
          artist: "Oasis",
          genre: "Rock",
          name: "Wonderwall",
        },
        {
          year: 2000,
          artist: "Radiohead",
          genre: "Alternative Rock",
          name: "Paranoid Android",
        },
        {
          year: 1999,
          artist: "Britney Spears",
          genre: "Pop",
          name: "...Baby One More Time",
        },
        {
          year: 1975,
          artist: "Queen",
          genre: "Rock",
          name: "Bohemian Rhapsody",
        },
        {
          year: 1967,
          artist: "The Beatles",
          genre: "Rock",
          name: "A Day in the Life",
        },
        {
          year: 1992,
          artist: "Dr. Dre ft. Snoop Dogg",
          genre: "Hip-Hop",
          name: "Nuthin' but a G Thang",
        },
      ]),

      ListofAdded: [],
      NewList: [],
    };
  },

  components: {
    MusicList,
    PlayList,
    SocialBox,
  },

  props: {
    Removed: {
      type: Array,
    },
    Rere: {
      type: Array,
    },
  },

  methods: {
    RemovedMusicData(RemoveRecieved) {
      this.ListofAdded = this.ListofAdded.filter(
        (item) => item !== RemoveRecieved
      );
      console.log(this.ListofAdded);
    },

    MusicDataFromChild(DataRecieved) {
      // Log Data From Child Component
      this.ListofAdded = DataRecieved;
      console.log(this.ListofAdded); // "Dummy Data"
    },
  },
};
</script>

<style>
.Center {
  text-align: center;
}
html {
  background-color: #282a2b;
  color: #ebe7e0;
}
section {
  display: flex;
  flex-direction: row;
}

body {
  display: flex;
  grid-template-columns: 1fr 1fr;
  padding: 0 2rem;
  place-items: center;
  justify-content: space-around;
  align-content: center;
}
</style>
