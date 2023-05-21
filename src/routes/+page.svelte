<script>
	import Cinema from "../components/Cinema.svelte";

	let cinemas = [
  {
    "name": "ABC",
    "address": "Herzogstr. 1",
    "phone": "089 / 33 23 00",
    "movies": [
      {
        "title": "Das Lehrerzimmer",
        "times": {
          "Monday": [],
          "Tuesday": ["19:30"],
          "Wednesday": ["19:30"],
          "Thursday": ["15:00"],
          "Friday": ["15:00"],
          "Saturday": ["15:00"],
          "Sunday": ["17:15"]
        },
        "reviews": ["artechock-Kritik", "artechock-Videokritik"]
      },
      {
        "title": "Living – Einmal wirklich leben",
        "times": {
          "Monday": ["19:30"],
          "Tuesday": [],
          "Wednesday": ["19:30"],
          "Thursday": ["17:15"],
          "Friday": [],
          "Saturday": ["17:15"],
          "Sunday": ["15:00"]
        },
        "reviews": []
      },
      {
        "title": "Living – Einmal wirklich leben (Living) (OmU)",
        "times": {
          "Monday": ["17:15"],
          "Tuesday": [],
          "Wednesday": ["17:15"],
          "Thursday": [],
          "Friday": [],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": []
      }
    ]
  },
  {
    "name": "Arena Filmtheater",
    "address": "Hans-Sachs-Straße 7",
    "phone": "089 / 260 32 65",
    "movies": [
      {
        "title": "Empire of Light (OmU)",
        "times": {
          "Monday": ["16:00"],
          "Tuesday": [],
          "Wednesday": ["18:15"],
          "Thursday": ["13:00"],
          "Friday": [],
          "Saturday": ["18:15"],
          "Sunday": []
        },
        "reviews": ["artechock-Kritik"]
      },
      {
        "title": "Adiós Buenos Aires",
        "times": {
          "Monday": ["20:45"],
          "Tuesday": ["20:45"],
          "Wednesday": ["20:45"],
          "Thursday": ["13:10", "18:45"],
          "Friday": [],
          "Saturday": ["16:50", "20:45"],
          "Sunday": ["20:45"]
        },
        "reviews": ["artechock-Kritik"]
      },
      {
        "title": "Adiós Buenos Aires (OmU)",
        "times": {
          "Monday": ["20:45"],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": [],
          "Friday": ["20:45"],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": ["artechock-Kritik"]
      },
      {
        "title": "Im Taxi mit Madeleine",
        "times": {
          "Monday": [],
          "Tuesday": ["16:50"],
          "Wednesday": [],
          "Thursday": ["15:00"],
          "Friday": ["16:50"],
          "Saturday": ["15:00"],
          "Sunday": ["15:00"]
        },
        "reviews": ["artechock-Kritik"]
      },
      {
        "title": "Im Taxi mit Madeleine (Une belle course) (OmU)",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": [],
          "Friday": ["16:50"],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": ["artechock-Kritik"]
      },
      {
        "title": "Oink",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": ["15:15"],
          "Friday": [],
          "Saturday": [],
          "Sunday": ["14:40"]
        },
        "reviews": ["artechock-Kritik"]
      },
      {
        "title": "Sparta",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": ["16:45"],
          "Friday": ["18:45"],
          "Saturday": ["18:45"],
          "Sunday": ["18:45"]
        },
        "reviews": ["artechock-Kritik"]
      },
      {
        "title": "Living – Einmal wirklich leben (Living) (OmU)",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": ["20:40"],
          "Friday": ["20:30"],
          "Saturday": ["16:10", "20:30"],
          "Sunday": ["20:30"]
        },
        "reviews": []
      },
      {
        "title": "Der Fuchs",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": ["16:00"],
          "Thursday": [],
          "Friday": [],
          "Saturday": ["18:15"],
          "Sunday": ["18:15"]
        },
        "reviews": ["artechock-Kritik"]
      },
      {
        "title": "Lars Eidinger – Sein oder nicht sein",
        "times": {
          "Monday": [],
          "Tuesday": ["16:20"],
          "Wednesday": [],
          "Thursday": [],
          "Friday": [],
          "Saturday": ["14:20"],
          "Sunday": []
        },
        "reviews": []
      },
      {
        "title": "Sisi & ich",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": [],
          "Friday": [],
          "Saturday": [],
          "Sunday": ["12:10"]
        },
        "reviews": ["artechock-Kritik"]
      },
      {
        "title": "Die Gewerk­schaf­terin",
        "times": {
          "Monday": [],
          "Tuesday": ["16:20"],
          "Wednesday": [],
          "Thursday": [],
          "Friday": [],
          "Saturday": [],
          "Sunday": ["12:30"]
        },
        "reviews": []
      },
      {
        "title": "Die Gewerk­schaf­terin (La syndi­ca­liste) (OmU)",
        "times": {
          "Monday": ["16:20"],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": [],
          "Friday": [],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": []
      },
      {
        "title": "Suzume (Suzume no tojimari) (OmeU)",
        "times": {
          "Monday": ["18:10"],
          "Tuesday": ["18:10"],
          "Wednesday": [],
          "Thursday": [],
          "Friday": [],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": ["artechock-Kritik"]
      },
      {
        "title": "No Goodbye",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": ["17:00 (Isar Fest­spiele)"],
          "Friday": [],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": []
      },
      {
        "title": "A Fine Line – Die Grat­wan­de­rung (OmU)",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": ["17:30 (Isar Fest­spiele)"],
          "Friday": [],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": []
      },
      {
        "title": "Maren",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": ["18:30 (Isar Fest­spiele)"],
          "Friday": [],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": []
      },
      {
        "title": "Augen­blick­lich Depres­sion",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": ["19:00 (Isar Fest­spiele)"],
          "Friday": [],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": []
      },
      {
        "title": "Irri­tieridi",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": ["19:10 (Isar Fest­spiele)"],
          "Friday": [],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": []
      },
      {
        "title": "Something That Sticks (OF)",
        "times": {
          "Monday": [],
          "Tuesday": [],
          "Wednesday": [],
          "Thursday": ["20:00 (Isar Fest­spiele)"],
          "Friday": [],
          "Saturday": [],
          "Sunday": []
        },
        "reviews": []
      }
    ]
  }
]
</script>

<h1>Munich Movie Showtimes</h1>

<div class="cinema-list">
	{#each cinemas as cinema}
		<Cinema {cinema}/>
	{/each}
</div>