# Examen_bases_de_datos


**Consultas sobre una tabla**

1. Obtener los nombres de todos los actores y las películas en las
que han actuado.

```mysql
select a.nombre, p.titulo
FROM actor as a
INNER JOIN pelicula_actor as pa ON pa.id_actor = a.id_actor
LEFT JOIN pelicula as p ON p.id_pelicula = pa.id_pelicula; 

+-------------+-----------------------------+
| nombre      | titulo                      |
+-------------+-----------------------------+
| PENELOPE    | ACADEMY DINOSAUR            |
| PENELOPE    | ANACONDA CONFESSIONS        |
| PENELOPE    | ANGELS LIFE                 |
| PENELOPE    | BULWORTH COMMANDMENTS       |
| PENELOPE    | CHEAPER CLYDE               |
| PENELOPE    | COLOR PHILADELPHIA          |
| PENELOPE    | ELEPHANT TROJAN             |
| PENELOPE    | GLEAMING JAWBREAKER         |
| PENELOPE    | HUMAN GRAFFITI              |
| PENELOPE    | KING EVOLUTION              |
| PENELOPE    | LADY STAGE                  |
| PENELOPE    | LANGUAGE COWBOY             |
| PENELOPE    | MULHOLLAND BEAST            |
| PENELOPE    | OKLAHOMA JUMANJI            |
| PENELOPE    | RULES HUMAN                 |
| PENELOPE    | SPLASH GUMP                 |
| PENELOPE    | VERTIGO NORTHWEST           |
| PENELOPE    | WESTWARD SEABISCUIT         |
| PENELOPE    | WIZARD COLDBLOODED          |
| NICK        | ADAPTATION HOLES            |
| NICK        | APACHE DIVINE               |
| NICK        | BABY HALL                   |
| NICK        | BULL SHAWSHANK              |
| NICK        | CHAINSAW UPTOWN             |
| NICK        | CHISUM BEHAVIOR             |
| NICK        | DESTINY SATURDAY            |
| NICK        | DRACULA CRYSTAL             |
| NICK        | FIGHT JAWBREAKER            |
| NICK        | FLASH WARS                  |
| NICK        | GILBERT PELICAN             |
| NICK        | GOODFELLAS SALUTE           |
| NICK        | HAPPINESS UNITED            |
| NICK        | INDIAN LOVE                 |
| NICK        | JEKYLL FROGMEN              |
| NICK        | JERSEY SASSY                |
| NICK        | LIAISONS SWEET              |
| NICK        | LUCKY FLYING                |
| NICK        | MAGUIRE APACHE              |
| NICK        | MALLRATS UNITED             |
| NICK        | MASK PEACH                  |
| NICK        | ROOF CHAMPION               |
| NICK        | RUSHMORE MERMAID            |
| NICK        | SMILE EARRING               |
| NICK        | WARDROBE PHANTOM            |
| ED          | ALONE TRIP                  |
| ED          | ARMY FLINTSTONES            |
| ED          | ARTIST COLDBLOODED          |
| ED          | BOONDOCK BALLROOM           |
| ED          | CADDYSHACK JEDI             |
| ED          | COWBOY DOOM                 |
| ED          | EVE RESURRECTION            |
| ED          | FORREST SONS                |
| ED          | FRENCH HOLIDAY              |
| ED          | FROST HEAD                  |
| ED          | HALLOWEEN NUTS              |
| ED          | HUNTER ALTER                |
| ED          | IMAGE PRINCESS              |
| ED          | JEEPERS WEDDING             |
| ED          | LUCK OPUS                   |
| ED          | NECKLACE OUTBREAK           |
| ED          | PLATOON INSTINCT            |
| ED          | SPICE SORORITY              |
| ED          | WEDDING APOLLO              |
| ED          | WEEKEND PERSONAL            |
| ED          | WHALE BIKINI                |
| ED          | YOUNG LANGUAGE              |
| JENNIFER    | ANACONDA CONFESSIONS        |
| JENNIFER    | ANGELS LIFE                 |
| JENNIFER    | BAREFOOT MANCHURIAN         |
| JENNIFER    | BED HIGHBALL                |
| JENNIFER    | BLADE POLISH                |
| JENNIFER    | BOONDOCK BALLROOM           |
| JENNIFER    | GHOSTBUSTERS ELF            |
| JENNIFER    | GREEDY ROOTS                |
| JENNIFER    | HANOVER GALAXY              |
| JENNIFER    | INSTINCT AIRPORT            |
| JENNIFER    | JUMANJI BLADE               |
| JENNIFER    | NATIONAL STORY              |
| JENNIFER    | OKLAHOMA JUMANJI            |
| JENNIFER    | POSEIDON FOREVER            |
| JENNIFER    | RAIDERS ANTITRUST           |
| JENNIFER    | RANDOM GO                   |
| JENNIFER    | REDS POCUS                  |
| JENNIFER    | SILVERADO GOLDFINGER        |
| JENNIFER    | SPLASH GUMP                 |
| JENNIFER    | SUBMARINE BED               |
| JENNIFER    | TREASURE COMMAND            |
| JENNIFER    | UNFORGIVEN ZOOLANDER        |
| JOHNNY      | AMADEUS HOLY                |
| JOHNNY      | BANGER PINOCCHIO            |
| JOHNNY      | BONNIE HOLOCAUST            |
| JOHNNY      | CHITTY LOCK                 |
| JOHNNY      | COMMANDMENTS EXPRESS        |
| JOHNNY      | CONEHEADS SMOOCHY           |
| JOHNNY      | DADDY PITTSBURGH            |
| JOHNNY      | DAISY MENAGERIE             |
| JOHNNY      | ENOUGH RAGING               |
| JOHNNY      | ESCAPE METROPOLIS           |
| JOHNNY      | FIRE WOLVES                 |
| JOHNNY      | FRONTIER CABIN              |
| JOHNNY      | GOODFELLAS SALUTE           |
| JOHNNY      | GRAIL FRANKENSTEIN          |
| JOHNNY      | GROOVE FICTION              |
| JOHNNY      | HALL CASSIDY                |
| JOHNNY      | HEAVENLY GUN                |
| JOHNNY      | KRAMER CHOCOLATE            |
| JOHNNY      | LOVE SUICIDES               |
| JOHNNY      | METAL ARMAGEDDON            |
| JOHNNY      | PACIFIC AMISTAD             |
| JOHNNY      | PATTON INTERVIEW            |
| JOHNNY      | POCUS PULP                  |
| JOHNNY      | RIDGEMONT SUBMARINE         |
| JOHNNY      | RINGS HEARTBREAKERS         |
| JOHNNY      | SMILE EARRING               |
| JOHNNY      | SOLDIERS EVOLUTION          |
| JOHNNY      | STAR OPERATION              |
| JOHNNY      | SUNRISE LEAGUE              |
| BETTE       | ANTITRUST TOMATOES          |
| BETTE       | BANG KWAI                   |
| BETTE       | BEAST HUNCHBACK             |
| BETTE       | BIKINI BORROWERS            |
| BETTE       | CALENDAR GUNFIGHT           |
| BETTE       | COAST RAINBOW               |
| BETTE       | COLDBLOODED DARLING         |
| BETTE       | CROSSROADS CASUALTIES       |
| BETTE       | DROP WATERFRONT             |
| BETTE       | IGBY MAKER                  |
| BETTE       | KRAMER CHOCOLATE            |
| BETTE       | LANGUAGE COWBOY             |
| BETTE       | LESSON CLEOPATRA            |
| BETTE       | LIBERTY MAGNIFICENT         |
| BETTE       | MULHOLLAND BEAST            |
| BETTE       | POTLUCK MIXED               |
| BETTE       | SPEED SUIT                  |
| BETTE       | TITANIC BOONDOCK            |
| BETTE       | TRADING PINOCCHIO           |
| BETTE       | WYOMING STORM               |
| GRACE       | ANGELS LIFE                 |
| GRACE       | ANONYMOUS HUMAN             |
| GRACE       | ARACHNOPHOBIA ROLLERCOASTER |
| GRACE       | BERETS AGENT                |
| GRACE       | BREAKING HOME               |
| GRACE       | COMMAND DARLING             |
| GRACE       | CONFESSIONS MAGUIRE         |
| GRACE       | DAZED PUNK                  |
| GRACE       | DECEIVER BETRAYED           |
| GRACE       | DESTINATION JERK            |
| GRACE       | EXCITEMENT EVE              |
| GRACE       | GASLIGHT CRUSADE            |
| GRACE       | HELLFIGHTERS SIERRA         |
| GRACE       | INSTINCT AIRPORT            |
| GRACE       | MALKOVICH PET               |
| GRACE       | NECKLACE OUTBREAK           |
| GRACE       | OCTOBER SUBMARINE           |
| GRACE       | OPEN AFRICAN                |
| GRACE       | POSEIDON FOREVER            |
| GRACE       | SAINTS BRIDE                |
| GRACE       | SAVANNAH TOWN               |
| GRACE       | SCISSORHANDS SLUMS          |
| GRACE       | SLEEPLESS MONSOON           |
| GRACE       | SLEEPY JAPANESE             |
| GRACE       | STING PERSONAL              |
| GRACE       | TOWN ARK                    |
| GRACE       | TRACY CIDER                 |
| GRACE       | TREATMENT JEKYLL            |
| GRACE       | WAR NOTTING                 |
| GRACE       | WARLOCK WEREWOLF            |
| MATTHEW     | BABY HALL                   |
| MATTHEW     | CAMPUS REMEMBER             |
| MATTHEW     | CLONES PINOCCHIO            |
| MATTHEW     | CONQUERER NUTS              |
| MATTHEW     | CROWDS TELEMARK             |
| MATTHEW     | DANCES NONE                 |
| MATTHEW     | DRIVING POLISH              |
| MATTHEW     | DURHAM PANKY                |
| MATTHEW     | FLASH WARS                  |
| MATTHEW     | HANGING DEEP                |
| MATTHEW     | INDIAN LOVE                 |
| MATTHEW     | LIGHTS DEER                 |
| MATTHEW     | LOSER HUSTLER               |
| MATTHEW     | MALKOVICH PET               |
| MATTHEW     | RUNNER MADIGAN              |
| MATTHEW     | SCHOOL JACKET               |
| MATTHEW     | SCORPION APOLLO             |
| MATTHEW     | SUGAR WONKA                 |
| MATTHEW     | TOMORROW HUSTLER            |
| MATTHEW     | VANISHING ROCKY             |
| JOE         | ANYTHING SAVANNAH           |
| JOE         | BIRCH ANTITRUST             |
| JOE         | CHOCOLAT HARRY              |
| JOE         | CHOCOLATE DUCK              |
| JOE         | CROOKED FROGMEN             |
| JOE         | CURTAIN VIDEOTAPE           |
| JOE         | DALMATIONS SWEDEN           |
| JOE         | HORROR REIGN                |
| JOE         | LAWLESS VISION              |
| JOE         | LEBOWSKI SOLDIERS           |
| JOE         | MAJESTIC FLOATS             |
| JOE         | PACIFIC AMISTAD             |
| JOE         | PERDITION FARGO             |
| JOE         | PRIMARY GLASS               |
| JOE         | REEF SALUTE                 |
| JOE         | RUNNER MADIGAN              |
| JOE         | SMILE EARRING               |
| JOE         | SNATCHERS MONTEZUMA         |
| JOE         | SUNRISE LEAGUE              |
| JOE         | SWEETHEARTS SUSPECTS        |
| JOE         | TIES HUNGER                 |
| JOE         | TRAFFIC HOBBIT              |
| JOE         | UNTOUCHABLES SUNRISE        |
| JOE         | WATERFRONT DELIVERANCE      |
| JOE         | WILD APOLLO                 |
| CHRISTIAN   | ACADEMY DINOSAUR            |
| CHRISTIAN   | ALABAMA DEVIL               |
| CHRISTIAN   | CROOKED FROGMEN             |
| CHRISTIAN   | DIVINE RESURRECTION         |
| CHRISTIAN   | DRAGONFLY STRANGERS         |
| CHRISTIAN   | GOLDFINGER SENSIBILITY      |
| CHRISTIAN   | JAWBREAKER BROOKLYN         |
| CHRISTIAN   | JEEPERS WEDDING             |
| CHRISTIAN   | LIFE TWISTED                |
| CHRISTIAN   | LORD ARIZONA                |
| CHRISTIAN   | MOD SECRETARY               |
| CHRISTIAN   | PREJUDICE OLEANDER          |
| CHRISTIAN   | PUNK DIVORCE                |
| CHRISTIAN   | REAP UNFAITHFUL             |
| CHRISTIAN   | SHAKESPEARE SADDLE          |
| CHRISTIAN   | TROUBLE DATE                |
| CHRISTIAN   | USUAL UNTOUCHABLES          |
| CHRISTIAN   | VACATION BOONDOCK           |
| CHRISTIAN   | WATERFRONT DELIVERANCE      |
| CHRISTIAN   | WEDDING APOLLO              |
| CHRISTIAN   | WIZARD COLDBLOODED          |
| CHRISTIAN   | WON DARES                   |
| ZERO        | CANYON STOCK                |
| ZERO        | DANCES NONE                 |
| ZERO        | ENCINO ELF                  |
| ZERO        | ENDING CROWDS               |
| ZERO        | GANDHI KWAI                 |
| ZERO        | GODFATHER DIARY             |
| ZERO        | HANDICAP BOONDOCK           |
| ZERO        | HONEY TIES                  |
| ZERO        | HORN WORKING                |
| ZERO        | IMAGE PRINCESS              |
| ZERO        | JERSEY SASSY                |
| ZERO        | LOSER HUSTLER               |
| ZERO        | MEET CHOCOLATE              |
| ZERO        | MOD SECRETARY               |
| ZERO        | MOONWALKER FOOL             |
| ZERO        | OLEANDER CLUE               |
| ZERO        | RACER EGG                   |
| ZERO        | STORY SIDE                  |
| ZERO        | STRANGERS GRAFFITI          |
| ZERO        | THIN SAGEBRUSH              |
| ZERO        | TOOTSIE PILOT               |
| ZERO        | UPTOWN YOUNG                |
| ZERO        | VELVET TERMINATOR           |
| ZERO        | WEST LION                   |
| ZERO        | WORKER TARZAN               |
| KARL        | ALLEY EVOLUTION             |
| KARL        | ALONE TRIP                  |
| KARL        | ARABIA DOGMA                |
| KARL        | ARIZONA BANG                |
| KARL        | BOUND CHEAPER               |
| KARL        | BOWFINGER GABLES            |
| KARL        | BUNCH MINDS                 |
| KARL        | CLEOPATRA DEVIL             |
| KARL        | CONNECTICUT TRAMP           |
| KARL        | DARES PLUTO                 |
| KARL        | DATE SPEED                  |
| KARL        | DAY UNFAITHFUL              |
| KARL        | DOORS PRESIDENT             |
| KARL        | FURY MURDER                 |
| KARL        | HARDLY ROBBERS              |
| KARL        | HIGHBALL POTTER             |
| KARL        | HOLES BRANNIGAN             |
| KARL        | INDEPENDENCE HOTEL          |
| KARL        | LEATHERNECKS DWARFS         |
| KARL        | LUCKY FLYING                |
| KARL        | MONTEREY LABYRINTH          |
| KARL        | NOVOCAINE FLIGHT            |
| KARL        | OKLAHOMA JUMANJI            |
| KARL        | PERFECT GROOVE              |
| KARL        | REAP UNFAITHFUL             |
| KARL        | REUNION WITCHES             |
| KARL        | SMOKING BARBARELLA          |
| KARL        | STAGECOACH ARMAGEDDON       |
| KARL        | SWEDEN SHINING              |
| KARL        | TELEMARK HEARTBREAKERS      |
| KARL        | VIRGINIAN PLUTO             |
| UMA         | ALONE TRIP                  |
| UMA         | ANTITRUST TOMATOES          |
| UMA         | ATTRACTION NEWTON           |
| UMA         | BOONDOCK BALLROOM           |
| UMA         | CABIN FLASH                 |
| UMA         | CHINATOWN GLADIATOR         |
| UMA         | CLASH FREDDY                |
| UMA         | CLUELESS BUCKET             |
| UMA         | DAISY MENAGERIE             |
| UMA         | DRIVER ANNIE                |
| UMA         | FRIDA SLIPPER               |
| UMA         | GALAXY SWEETHEARTS          |
| UMA         | GRINCH MASSAGE              |
| UMA         | GROUNDHOG UNCUT             |
| UMA         | HOMEWARD CIDER              |
| UMA         | INCH JET                    |
| UMA         | LEATHERNECKS DWARFS         |
| UMA         | LEGALLY SECRETARY           |
| UMA         | LIFE TWISTED                |
| UMA         | LION UNCUT                  |
| UMA         | LOLITA WORLD                |
| UMA         | METAL ARMAGEDDON            |
| UMA         | MODEL FISH                  |
| UMA         | MOONWALKER FOOL             |
| UMA         | MOTIONS DETAILS             |
| UMA         | REBEL AIRPORT               |
| UMA         | RIDER CADDYSHACK            |
| UMA         | SNOWMAN ROLLERCOASTER       |
| UMA         | SOLDIERS EVOLUTION          |
| UMA         | SPLASH GUMP                 |
| UMA         | SPLENDOR PATTON             |
| UMA         | STEEL SANTA                 |
| UMA         | TORQUE BOUND                |
| UMA         | WEDDING APOLLO              |
| UMA         | ZHIVAGO CORE                |
| VIVIEN      | CLASH FREDDY                |
| VIVIEN      | CRANES RESERVOIR            |
| VIVIEN      | DIRTY ACE                   |
| VIVIEN      | DONNIE ALLEY                |
| VIVIEN      | DRIFTER COMMANDMENTS        |
| VIVIEN      | DRIVING POLISH              |
| VIVIEN      | DRUMS DYNAMITE              |
| VIVIEN      | ENEMY ODDS                  |
| VIVIEN      | EXCITEMENT EVE              |
| VIVIEN      | GORGEOUS BINGO              |
| VIVIEN      | HIGH ENCINO                 |
| VIVIEN      | HILLS NEIGHBORS             |
| VIVIEN      | HOBBIT ALIEN                |
| VIVIEN      | IMPACT ALADDIN              |
| VIVIEN      | ITALIAN AFRICAN             |
| VIVIEN      | JAPANESE RUN                |
| VIVIEN      | KENTUCKIAN GIANT            |
| VIVIEN      | LOVELY JINGLE               |
| VIVIEN      | LOVER TRUMAN                |
| VIVIEN      | MUSSOLINI SPOILERS          |
| VIVIEN      | POLISH BROOKLYN             |
| VIVIEN      | SALUTE APOLLO               |
| VIVIEN      | SATURDAY LAMBS              |
| VIVIEN      | STOCK GLASS                 |
| VIVIEN      | STREETCAR INTENTIONS        |
| VIVIEN      | TIGHTS DAWN                 |
| VIVIEN      | TRAP GUYS                   |
| VIVIEN      | TYCOON GATHERING            |
| VIVIEN      | VOICE PEACH                 |
| VIVIEN      | WESTWARD SEABISCUIT         |
| CUBA        | APACHE DIVINE               |
| CUBA        | BORROWERS BEDAZZLED         |
| CUBA        | BOUND CHEAPER               |
| CUBA        | BUTCH PANTHER               |
| CUBA        | CASSIDY WYOMING             |
| CUBA        | DIVINE RESURRECTION         |
| CUBA        | EGYPT TENENBAUMS            |
| CUBA        | EMPIRE MALKOVICH            |
| CUBA        | FLYING HOOK                 |
| CUBA        | FUGITIVE MAGUIRE            |
| CUBA        | HELLFIGHTERS SIERRA         |
| CUBA        | HYDE DOCTOR                 |
| CUBA        | KISS GLORY                  |
| CUBA        | KNOCK WARLOCK               |
| CUBA        | LUKE MUMMY                  |
| CUBA        | MAKER GABLES                |
| CUBA        | MONTEZUMA COMMAND           |
| CUBA        | NOON PAPI                   |
| CUBA        | OKLAHOMA JUMANJI            |
| CUBA        | ROSES TREASURE              |
| CUBA        | SHANE DARKNESS              |
| CUBA        | SIEGE MADRE                 |
| CUBA        | SOLDIERS EVOLUTION          |
| CUBA        | THEORY MERMAID              |
| CUBA        | UNFORGIVEN ZOOLANDER        |
| CUBA        | VOLCANO TEXAS               |
| CUBA        | WEREWOLF LOLA               |
| CUBA        | WONDERLAND CHRISTMAS        |
| FRED        | BLANKET BEVERLY             |
| FRED        | BOONDOCK BALLROOM           |
| FRED        | BROTHERHOOD BLANKET         |
| FRED        | CAROL TEXAS                 |
| FRED        | CLEOPATRA DEVIL             |
| FRED        | CONNECTICUT TRAMP           |
| FRED        | DECEIVER BETRAYED           |
| FRED        | DELIVERANCE MULHOLLAND      |
| FRED        | EAGLES PANKY                |
| FRED        | EARRING INSTINCT            |
| FRED        | EASY GLADIATOR              |
| FRED        | EMPIRE MALKOVICH            |
| FRED        | ENTRAPMENT SATISFACTION     |
| FRED        | GABLES METROPOLIS           |
| FRED        | HUMAN GRAFFITI              |
| FRED        | IMAGE PRINCESS              |
| FRED        | IMPOSSIBLE PREJUDICE        |
| FRED        | INCH JET                    |
| FRED        | KRAMER CHOCOLATE            |
| FRED        | MAGNIFICENT CHITTY          |
| FRED        | MIRACLE VIRTUAL             |
| FRED        | MISSION ZOOLANDER           |
| FRED        | REAR TRADING                |
| FRED        | SAINTS BRIDE                |
| FRED        | SENSE GREEK                 |
| FRED        | THEORY MERMAID              |
| FRED        | WEEKEND PERSONAL            |
| HELEN       | BREAKING HOME               |
| HELEN       | CAPER MOTIONS               |
| HELEN       | CASPER DRAGONFLY            |
| HELEN       | CAT CONEHEADS               |
| HELEN       | CLASH FREDDY                |
| HELEN       | CUPBOARD SINNERS            |
| HELEN       | CYCLONE FAMILY              |
| HELEN       | DIVINE RESURRECTION         |
| HELEN       | EMPIRE MALKOVICH            |
| HELEN       | FEVER EMPIRE                |
| HELEN       | FIDELITY DEVIL              |
| HELEN       | GREATEST NORTH              |
| HELEN       | INDEPENDENCE HOTEL          |
| HELEN       | IRON MOON                   |
| HELEN       | JAWS HARRY                  |
| HELEN       | KISS GLORY                  |
| HELEN       | LEGALLY SECRETARY           |
| HELEN       | LIES TREATMENT              |
| HELEN       | MICROCOSMOS PARADISE        |
| HELEN       | MOVIE SHAKESPEARE           |
| HELEN       | MUMMY CREATURES             |
| HELEN       | ROAD ROXANNE                |
| HELEN       | SCISSORHANDS SLUMS          |
| HELEN       | SIDE ARK                    |
| HELEN       | SINNERS ATLANTIS            |
| HELEN       | STRANGER STRANGERS          |
| HELEN       | SWEETHEARTS SUSPECTS        |
| HELEN       | TADPOLE PARK                |
| HELEN       | TELEMARK HEARTBREAKERS      |
| HELEN       | VOICE PEACH                 |
| HELEN       | WAR NOTTING                 |
| HELEN       | WARLOCK WEREWOLF            |
| DAN         | ATTACKS HATE                |
| DAN         | BOILED DARES                |
| DAN         | CHINATOWN GLADIATOR         |
| DAN         | CONEHEADS SMOOCHY           |
| DAN         | EARLY HOME                  |
| DAN         | ELIZABETH SHANE             |
| DAN         | EMPIRE MALKOVICH            |
| DAN         | FLASH WARS                  |
| DAN         | GUMP DATE                   |
| DAN         | INNOCENT USUAL              |
| DAN         | INSIDER ARIZONA             |
| DAN         | JERK PAYCHECK               |
| DAN         | LOVELY JINGLE               |
| DAN         | MASK PEACH                  |
| DAN         | MUSSOLINI SPOILERS          |
| DAN         | REAR TRADING                |
| DAN         | SLING LUKE                  |
| DAN         | STATE WASTELAND             |
| DAN         | SUN CONFESSIONS             |
| DAN         | TEQUILA PAST                |
| DAN         | TUXEDO MILE                 |
| DAN         | VIRGIN DAISY                |
| BOB         | ACE GOLDFINGER              |
| BOB         | ADAPTATION HOLES            |
| BOB         | CHINATOWN GLADIATOR         |
| BOB         | CIRCUS YOUTH                |
| BOB         | CONTROL ANTHEM              |
| BOB         | DARES PLUTO                 |
| BOB         | DARN FORRESTER              |
| BOB         | DAZED PUNK                  |
| BOB         | DYNAMITE TARZAN             |
| BOB         | HATE HANDICAP               |
| BOB         | HOMICIDE PEACH              |
| BOB         | JACKET FRISCO               |
| BOB         | JUMANJI BLADE               |
| BOB         | LAWLESS VISION              |
| BOB         | LEATHERNECKS DWARFS         |
| BOB         | OSCAR GOLD                  |
| BOB         | PELICAN COMFORTS            |
| BOB         | PERSONAL LADYBUGS           |
| BOB         | RAGING AIRPLANE             |
| BOB         | RUN PACIFIC                 |
| BOB         | RUNNER MADIGAN              |
| BOB         | SADDLE ANTITRUST            |
| BOB         | SCORPION APOLLO             |
| BOB         | SHAWSHANK BUBBLE            |
| BOB         | TAXI KICK                   |
| LUCILLE     | ACADEMY DINOSAUR            |
| LUCILLE     | BANGER PINOCCHIO            |
| LUCILLE     | BEDAZZLED MARRIED           |
| LUCILLE     | CHEAPER CLYDE               |
| LUCILLE     | CHITTY LOCK                 |
| LUCILLE     | COLDBLOODED DARLING         |
| LUCILLE     | DINOSAUR SECRETARY          |
| LUCILLE     | DOORS PRESIDENT             |
| LUCILLE     | EARRING INSTINCT            |
| LUCILLE     | EGG IGBY                    |
| LUCILLE     | GANDHI KWAI                 |
| LUCILLE     | GOLDFINGER SENSIBILITY      |
| LUCILLE     | HYDE DOCTOR                 |
| LUCILLE     | JAWS HARRY                  |
| LUCILLE     | JUNGLE CLOSER               |
| LUCILLE     | KING EVOLUTION              |
| LUCILLE     | LOLA AGENT                  |
| LUCILLE     | LOSE INCH                   |
| LUCILLE     | LOVERBOY ATTACKS            |
| LUCILLE     | MODERN DORADO               |
| LUCILLE     | ORIENT CLOSER               |
| LUCILLE     | PAJAMA JAWBREAKER           |
| LUCILLE     | PATIENT SISTER              |
| LUCILLE     | RANDOM GO                   |
| LUCILLE     | REAR TRADING                |
| LUCILLE     | SAGEBRUSH CLUELESS          |
| LUCILLE     | SHANGHAI TYCOON             |
| LUCILLE     | SUN CONFESSIONS             |
| LUCILLE     | WASTELAND DIVINE            |
| LUCILLE     | WINDOW SIDE                 |
| KIRSTEN     | AGENT TRUMAN                |
| KIRSTEN     | BOONDOCK BALLROOM           |
| KIRSTEN     | BORN SPINAL                 |
| KIRSTEN     | CHICKEN HELLFIGHTERS        |
| KIRSTEN     | CLOSER BANG                 |
| KIRSTEN     | CONQUERER NUTS              |
| KIRSTEN     | DRIFTER COMMANDMENTS        |
| KIRSTEN     | ENCINO ELF                  |
| KIRSTEN     | FLASH WARS                  |
| KIRSTEN     | HANOVER GALAXY              |
| KIRSTEN     | HOME PITY                   |
| KIRSTEN     | HONEY TIES                  |
| KIRSTEN     | KILL BROTHERHOOD            |
| KIRSTEN     | LADYBUGS ARMAGEDDON         |
| KIRSTEN     | LORD ARIZONA                |
| KIRSTEN     | PINOCCHIO SIMON             |
| KIRSTEN     | PLUTO OLEANDER              |
| KIRSTEN     | PRIX UNDEFEATED             |
| KIRSTEN     | PULP BEVERLY                |
| KIRSTEN     | RIVER OUTLAW                |
| KIRSTEN     | ROAD ROXANNE                |
| KIRSTEN     | SILVERADO GOLDFINGER        |
| KIRSTEN     | SLEEPING SUSPECTS           |
| KIRSTEN     | THIEF PELICAN               |
| KIRSTEN     | TITANS JERK                 |
| KIRSTEN     | UNBREAKABLE KARATE          |
| KIRSTEN     | WON DARES                   |
| ELVIS       | ALABAMA DEVIL               |
| ELVIS       | ANACONDA CONFESSIONS        |
| ELVIS       | BAREFOOT MANCHURIAN         |
| ELVIS       | BORROWERS BEDAZZLED         |
| ELVIS       | CADDYSHACK JEDI             |
| ELVIS       | CHITTY LOCK                 |
| ELVIS       | EVOLUTION ALTER             |
| ELVIS       | EXPECATIONS NATURAL         |
| ELVIS       | GANGS PRIDE                 |
| ELVIS       | GOODFELLAS SALUTE           |
| ELVIS       | HOBBIT ALIEN                |
| ELVIS       | HOOK CHARIOTS               |
| ELVIS       | JERICHO MULAN               |
| ELVIS       | JUMPING WRATH               |
| ELVIS       | KENTUCKIAN GIANT            |
| ELVIS       | LOVELY JINGLE               |
| ELVIS       | MOTIONS DETAILS             |
| ELVIS       | ODDS BOOGIE                 |
| ELVIS       | OUTLAW HANKY                |
| ELVIS       | POLISH BROOKLYN             |
| ELVIS       | RIGHT CRANES                |
| ELVIS       | ROOF CHAMPION               |
| ELVIS       | SEATTLE EXPECATIONS         |
| ELVIS       | SKY MIRACLE                 |
| ELVIS       | TROJAN TOMORROW             |
| ELVIS       | WATERFRONT DELIVERANCE      |
| SANDRA      | AGENT TRUMAN                |
| SANDRA      | ARTIST COLDBLOODED          |
| SANDRA      | BLACKOUT PRIVATE            |
| SANDRA      | BULL SHAWSHANK              |
| SANDRA      | CANDIDATE PERDITION         |
| SANDRA      | CANDLES GRAPES              |
| SANDRA      | CASSIDY WYOMING             |
| SANDRA      | DARN FORRESTER              |
| SANDRA      | DESTINY SATURDAY            |
| SANDRA      | DIVIDE MONSTER              |
| SANDRA      | DRIVER ANNIE                |
| SANDRA      | GOLDMINE TYCOON             |
| SANDRA      | GORGEOUS BINGO              |
| SANDRA      | HELLFIGHTERS SIERRA         |
| SANDRA      | HOCUS FRIDA                 |
| SANDRA      | HOTEL HAPPINESS             |
| SANDRA      | IDENTITY LOVER              |
| SANDRA      | JUMPING WRATH               |
| SANDRA      | LOVELY JINGLE               |
| SANDRA      | MAGNOLIA FORRESTER          |
| SANDRA      | OLEANDER CLUE               |
| SANDRA      | OZ LIAISONS                 |
| SANDRA      | PERSONAL LADYBUGS           |
| SANDRA      | POSEIDON FOREVER            |
| SANDRA      | SAVANNAH TOWN               |
| SANDRA      | SHAKESPEARE SADDLE          |
| SANDRA      | SLEEPING SUSPECTS           |
| SANDRA      | SONS INTERVIEW              |
| SANDRA      | SPEED SUIT                  |
| SANDRA      | SPLENDOR PATTON             |
| SANDRA      | STATE WASTELAND             |
| SANDRA      | STRANGER STRANGERS          |
| SANDRA      | STREAK RIDGEMONT            |
| SANDRA      | STREETCAR INTENTIONS        |
| SANDRA      | VANISHED GARDEN             |
| SANDRA      | WOLVES DESIRE               |
| SANDRA      | YOUTH KICK                  |
| CAMERON     | ADAPTATION HOLES            |
| CAMERON     | BLUES INSTINCT              |
| CAMERON     | CALENDAR GUNFIGHT           |
| CAMERON     | CASUALTIES ENCINO           |
| CAMERON     | CHOCOLATE DUCK              |
| CAMERON     | COAST RAINBOW               |
| CAMERON     | CONNECTION MICROCOSMOS      |
| CAMERON     | CROW GREASE                 |
| CAMERON     | CUPBOARD SINNERS            |
| CAMERON     | DOOM DANCING                |
| CAMERON     | DROP WATERFRONT             |
| CAMERON     | ELEPHANT TROJAN             |
| CAMERON     | FREEDOM CLEOPATRA           |
| CAMERON     | HAUNTED ANTITRUST           |
| CAMERON     | INSTINCT AIRPORT            |
| CAMERON     | LEGALLY SECRETARY           |
| CAMERON     | MOB DUFFEL                  |
| CAMERON     | MOVIE SHAKESPEARE           |
| CAMERON     | PANIC CLUB                  |
| CAMERON     | PURE RUNNER                 |
| CAMERON     | SEVEN SWARM                 |
| CAMERON     | SPINAL ROCKY                |
| CAMERON     | SPLASH GUMP                 |
| CAMERON     | WEST LION                   |
| KEVIN       | AMERICAN CIRCUS             |
| KEVIN       | BOOGIE AMELIE               |
| KEVIN       | CITIZEN SHREK               |
| KEVIN       | CONQUERER NUTS              |
| KEVIN       | DALMATIONS SWEDEN           |
| KEVIN       | DATE SPEED                  |
| KEVIN       | DESTINY SATURDAY            |
| KEVIN       | DOUBLE WRATH                |
| KEVIN       | FICTION CHRISTMAS           |
| KEVIN       | HATE HANDICAP               |
| KEVIN       | HEAVENLY GUN                |
| KEVIN       | HOLES BRANNIGAN             |
| KEVIN       | LOVERBOY ATTACKS            |
| KEVIN       | MASSAGE IMAGE               |
| KEVIN       | MISSION ZOOLANDER           |
| KEVIN       | MUMMY CREATURES             |
| KEVIN       | POLISH BROOKLYN             |
| KEVIN       | PRIMARY GLASS               |
| KEVIN       | SABRINA MIDNIGHT            |
| KEVIN       | SWEDEN SHINING              |
| KEVIN       | TROUBLE DATE                |
| RIP         | ALABAMA DEVIL               |
| RIP         | AMERICAN CIRCUS             |
| RIP         | ARABIA DOGMA                |
| RIP         | BOULEVARD MOB               |
| RIP         | BRANNIGAN SUNRISE           |
| RIP         | BUCKET BROTHERHOOD          |
| RIP         | CHOCOLAT HARRY              |
| RIP         | CRAFT OUTFIELD              |
| RIP         | CYCLONE FAMILY              |
| RIP         | DESTINATION JERK            |
| RIP         | DONNIE ALLEY                |
| RIP         | FOOL MOCKINGBIRD            |
| RIP         | FORREST SONS                |
| RIP         | FRONTIER CABIN              |
| RIP         | GABLES METROPOLIS           |
| RIP         | GUYS FALCON                 |
| RIP         | HALL CASSIDY                |
| RIP         | LONELY ELEPHANT             |
| RIP         | MADISON TRAP                |
| RIP         | MASSAGE IMAGE               |
| RIP         | OKLAHOMA JUMANJI            |
| RIP         | OSCAR GOLD                  |
| RIP         | PITTSBURGH HUNCHBACK        |
| RIP         | POLISH BROOKLYN             |
| RIP         | RANGE MOONWALKER            |
| RIP         | RINGS HEARTBREAKERS         |
| RIP         | SAINTS BRIDE                |
| RIP         | SATURDAY LAMBS              |
| RIP         | SIEGE MADRE                 |
| RIP         | SORORITY QUEEN              |
| RIP         | TEXAS WATCH                 |
| RIP         | TRAIN BUNCH                 |
| RIP         | TRAMP OTHERS                |
| JULIA       | AMADEUS HOLY                |
| JULIA       | ARABIA DOGMA                |
| JULIA       | BONNIE HOLOCAUST            |
| JULIA       | CIDER DESIRE                |
| JULIA       | CONEHEADS SMOOCHY           |
| JULIA       | EFFECT GLADIATOR            |
| JULIA       | FREDDY STORM                |
| JULIA       | GAMES BOWFINGER             |
| JULIA       | GLADIATOR WESTWARD          |
| JULIA       | HANOVER GALAXY              |
| JULIA       | HIGH ENCINO                 |
| JULIA       | INSIDER ARIZONA             |
| JULIA       | JAWBREAKER BROOKLYN         |
| JULIA       | KISS GLORY                  |
| JULIA       | KRAMER CHOCOLATE            |
| JULIA       | LUCKY FLYING                |
| JULIA       | MOCKINGBIRD HOLLYWOOD       |
| JULIA       | MONTEREY LABYRINTH          |
| JULIA       | OPEN AFRICAN                |
| JULIA       | PILOT HOOSIERS              |
| JULIA       | PITTSBURGH HUNCHBACK        |
| JULIA       | PRESIDENT BANG              |
| JULIA       | SCORPION APOLLO             |
| JULIA       | SLEEPLESS MONSOON           |
| JULIA       | SPIRIT FLINTSTONES          |
| JULIA       | STRANGERS GRAFFITI          |
| JULIA       | SWEETHEARTS SUSPECTS        |
| JULIA       | TELEMARK HEARTBREAKERS      |
| JULIA       | TIES HUNGER                 |
| JULIA       | TRAIN BUNCH                 |
| JULIA       | WEEKEND PERSONAL            |
| JULIA       | WONKA SEA                   |
| JULIA       | YOUNG LANGUAGE              |
| WOODY       | ALICE FANTASIA              |
| WOODY       | ATLANTIS CAUSE              |
| WOODY       | BEACH HEARTBREAKERS         |
| WOODY       | BIRCH ANTITRUST             |
| WOODY       | BREAKING HOME               |
| WOODY       | BUNCH MINDS                 |
| WOODY       | DUCK RACER                  |
| WOODY       | DURHAM PANKY                |
| WOODY       | ENTRAPMENT SATISFACTION     |
| WOODY       | GILMORE BOILED              |
| WOODY       | KNOCK WARLOCK               |
| WOODY       | LAMBS CINCINATTI            |
| WOODY       | LOSER HUSTLER               |
| WOODY       | MAIDEN HOME                 |
| WOODY       | MIDNIGHT WESTWARD           |
| WOODY       | MOONWALKER FOOL             |
| WOODY       | NEIGHBORS CHARADE           |
| WOODY       | NONE SPIKING                |
| WOODY       | PAJAMA JAWBREAKER           |
| WOODY       | PILOT HOOSIERS              |
| WOODY       | ROOM ROMAN                  |
| WOODY       | SHOOTIST SUPERFLY           |
| WOODY       | SHRUNK DIVINE               |
| WOODY       | SNOWMAN ROLLERCOASTER       |
| WOODY       | SPICE SORORITY              |
| WOODY       | SPY MILE                    |
| WOODY       | TELEGRAPH VOYAGE            |
| WOODY       | TRAP GUYS                   |
| WOODY       | WAIT CIDER                  |
| WOODY       | WIFE TURN                   |
| WOODY       | WYOMING STORM               |
| ALEC        | ALADDIN CALENDAR            |
| ALEC        | BLADE POLISH                |
| ALEC        | BULL SHAWSHANK              |
| ALEC        | CABIN FLASH                 |
| ALEC        | CENTER DINOSAUR             |
| ALEC        | CHAMBER ITALIAN             |
| ALEC        | CONEHEADS SMOOCHY           |
| ALEC        | DESTINY SATURDAY            |
| ALEC        | EFFECT GLADIATOR            |
| ALEC        | ENCOUNTERS CURTAIN          |
| ALEC        | EXPRESS LONELY              |
| ALEC        | FICTION CHRISTMAS           |
| ALEC        | FREEDOM CLEOPATRA           |
| ALEC        | FUGITIVE MAGUIRE            |
| ALEC        | HOURS RAGE                  |
| ALEC        | HUSTLER PARTY               |
| ALEC        | IDENTITY LOVER              |
| ALEC        | INSIDER ARIZONA             |
| ALEC        | JEOPARDY ENCINO             |
| ALEC        | JOON NORTHWEST              |
| ALEC        | LIBERTY MAGNIFICENT         |
| ALEC        | MAGIC MALLRATS              |
| ALEC        | MONEY HAROLD                |
| ALEC        | OUTBREAK DIVINE             |
| ALEC        | REIGN GENTLEMEN             |
| ALEC        | SMOKING BARBARELLA          |
| ALEC        | SUMMER SCARFACE             |
| ALEC        | UPTOWN YOUNG                |
| ALEC        | VIRGIN DAISY                |
| SANDRA      | ACADEMY DINOSAUR            |
| SANDRA      | BANG KWAI                   |
| SANDRA      | BEETHOVEN EXORCIST          |
| SANDRA      | BEVERLY OUTLAW              |
| SANDRA      | BIRDS PERDITION             |
| SANDRA      | BOONDOCK BALLROOM           |
| SANDRA      | DUDE BLINDNESS              |
| SANDRA      | DUMBO LUST                  |
| SANDRA      | ENOUGH RAGING               |
| SANDRA      | EXCITEMENT EVE              |
| SANDRA      | FAMILY SWEET                |
| SANDRA      | FIREHOUSE VIETNAM           |
| SANDRA      | FLASH WARS                  |
| SANDRA      | GILBERT PELICAN             |
| SANDRA      | MATRIX SNOWMAN              |
| SANDRA      | RINGS HEARTBREAKERS         |
| SANDRA      | SILENCE KANE                |
| SANDRA      | STAGECOACH ARMAGEDDON       |
| SANDRA      | VIRGINIAN PLUTO             |
| SISSY       | BORN SPINAL                 |
| SISSY       | CHITTY LOCK                 |
| SISSY       | CLYDE THEORY                |
| SISSY       | COAST RAINBOW               |
| SISSY       | CRAZY HOME                  |
| SISSY       | FACTORY DRAGON              |
| SISSY       | FERRIS MOTHER               |
| SISSY       | GONE TROUBLE                |
| SISSY       | GREEK EVERYONE              |
| SISSY       | HOOSIERS BIRDCAGE           |
| SISSY       | MOB DUFFEL                  |
| SISSY       | OPEN AFRICAN                |
| SISSY       | PRIX UNDEFEATED             |
| SISSY       | ROCKY WAR                   |
| SISSY       | SHRUNK DIVINE               |
| SISSY       | SKY MIRACLE                 |
| SISSY       | TELEMARK HEARTBREAKERS      |
| SISSY       | WISDOM WORKER               |
| TIM         | BEHAVIOR RUNAWAY            |
| TIM         | BOILED DARES                |
| TIM         | BUCKET BROTHERHOOD          |
| TIM         | CALENDAR GUNFIGHT           |
| TIM         | CHAPLIN LICENSE             |
| TIM         | CRUSADE HONEY               |
| TIM         | CUPBOARD SINNERS            |
| TIM         | DEEP CRUSADE                |
| TIM         | FEUD FROGMEN                |
| TIM         | FIDDLER LOST                |
| TIM         | HAROLD FRENCH               |
| TIM         | HOMEWARD CIDER              |
| TIM         | HOOSIERS BIRDCAGE           |
| TIM         | LIGHTS DEER                 |
| TIM         | MEET CHOCOLATE              |
| TIM         | MOB DUFFEL                  |
| TIM         | MUMMY CREATURES             |
| TIM         | PACKER MADIGAN              |
| TIM         | PEACH INNOCENT              |
| TIM         | PEARL DESTINY               |
| TIM         | SNATCHERS MONTEZUMA         |
| TIM         | UPTOWN YOUNG                |
| TIM         | WIZARD COLDBLOODED          |
| MILLA       | BAREFOOT MANCHURIAN         |
| MILLA       | CALENDAR GUNFIGHT           |
| MILLA       | CHANCE RESURRECTION         |
| MILLA       | CLASH FREDDY                |
| MILLA       | DAUGHTER MADIGAN            |
| MILLA       | DREAM PICKUP                |
| MILLA       | FATAL HAUNTED               |
| MILLA       | FEATHERS METAL              |
| MILLA       | JACKET FRISCO               |
| MILLA       | JUGGLER HARDLY              |
| MILLA       | MIDNIGHT WESTWARD           |
| MILLA       | NECKLACE OUTBREAK           |
| MILLA       | PEACH INNOCENT              |
| MILLA       | PREJUDICE OLEANDER          |
| MILLA       | RAIDERS ANTITRUST           |
| MILLA       | ROBBERS JOON                |
| MILLA       | ROCK INSTINCT               |
| MILLA       | RUSHMORE MERMAID            |
| MILLA       | SEATTLE EXPECATIONS         |
| MILLA       | TEEN APOLLO                 |
| MILLA       | TEMPLE ATTRACTION           |
| MILLA       | WATERSHIP FRONTIER          |
| MILLA       | WHISPERER GIANT             |
| MILLA       | WRONG BEHAVIOR              |
| AUDREY      | ATLANTIS CAUSE              |
| AUDREY      | BOULEVARD MOB               |
| AUDREY      | CAPER MOTIONS               |
| AUDREY      | CASSIDY WYOMING             |
| AUDREY      | CONEHEADS SMOOCHY           |
| AUDREY      | CONTROL ANTHEM              |
| AUDREY      | DORADO NOTTING              |
| AUDREY      | FRENCH HOLIDAY              |
| AUDREY      | GUNFIGHTER MUSSOLINI        |
| AUDREY      | HALLOWEEN NUTS              |
| AUDREY      | HUMAN GRAFFITI              |
| AUDREY      | KANE EXORCIST               |
| AUDREY      | KNOCK WARLOCK               |
| AUDREY      | LOATHING LEGALLY            |
| AUDREY      | PEAK FOREVER                |
| AUDREY      | REDEMPTION COMFORTS         |
| AUDREY      | SENSE GREEK                 |
| AUDREY      | SHIP WONDERLAND             |
| AUDREY      | SIDE ARK                    |
| AUDREY      | SQUAD FISH                  |
| AUDREY      | STING PERSONAL              |
| AUDREY      | STRANGER STRANGERS          |
| AUDREY      | USUAL UNTOUCHABLES          |
| AUDREY      | VOLUME HOUSE                |
| AUDREY      | WHALE BIKINI                |
| JUDY        | ALADDIN CALENDAR            |
| JUDY        | ARACHNOPHOBIA ROLLERCOASTER |
| JUDY        | BALLROOM MOCKINGBIRD        |
| JUDY        | CYCLONE FAMILY              |
| JUDY        | DROP WATERFRONT             |
| JUDY        | GUNFIGHTER MUSSOLINI        |
| JUDY        | MODERN DORADO               |
| JUDY        | MUSSOLINI SPOILERS          |
| JUDY        | NASH CHOCOLAT               |
| JUDY        | QUEST MUSSOLINI             |
| JUDY        | RINGS HEARTBREAKERS         |
| JUDY        | ROCKETEER MOTHER            |
| JUDY        | RUGRATS SHAKESPEARE         |
| JUDY        | SOLDIERS EVOLUTION          |
| JUDY        | TROUBLE DATE                |
| BURT        | ALIEN CENTER                |
| BURT        | BLINDNESS GUN               |
| BURT        | COMMANDMENTS EXPRESS        |
| BURT        | DINOSAUR SECRETARY          |
| BURT        | DOUBLE WRATH                |
| BURT        | ENDING CROWDS               |
| BURT        | GREEK EVERYONE              |
| BURT        | GRINCH MASSAGE              |
| BURT        | GUN BONNIE                  |
| BURT        | GUYS FALCON                 |
| BURT        | HEAVEN FREEDOM              |
| BURT        | HOME PITY                   |
| BURT        | HOMEWARD CIDER              |
| BURT        | IMAGE PRINCESS              |
| BURT        | INTOLERABLE INTENTIONS      |
| BURT        | JERK PAYCHECK               |
| BURT        | KANE EXORCIST               |
| BURT        | KING EVOLUTION              |
| BURT        | MENAGERIE RUSHMORE          |
| BURT        | MONEY HAROLD                |
| BURT        | MOTIONS DETAILS             |
| BURT        | RANDOM GO                   |
| BURT        | RANGE MOONWALKER            |
| BURT        | REAP UNFAITHFUL             |
| BURT        | RIGHT CRANES                |
| BURT        | TALENTED HOMICIDE           |
| BURT        | TRUMAN CRAZY                |
| BURT        | VALENTINE VANISHING         |
| BURT        | WANDA CHAMBER               |
| VAL         | ALADDIN CALENDAR            |
| VAL         | ALASKA PHANTOM              |
| VAL         | AMADEUS HOLY                |
| VAL         | CANYON STOCK                |
| VAL         | CAPER MOTIONS               |
| VAL         | CARRIE BUNCH                |
| VAL         | CHITTY LOCK                 |
| VAL         | DALMATIONS SWEDEN           |
| VAL         | DRIFTER COMMANDMENTS        |
| VAL         | DUDE BLINDNESS              |
| VAL         | ELEPHANT TROJAN             |
| VAL         | FIREBALL PHILADELPHIA       |
| VAL         | INTRIGUE WORST              |
| VAL         | JAWBREAKER BROOKLYN         |
| VAL         | JERSEY SASSY                |
| VAL         | LAMBS CINCINATTI            |
| VAL         | LONELY ELEPHANT             |
| VAL         | MAKER GABLES                |
| VAL         | MALLRATS UNITED             |
| VAL         | METROPOLIS COMA             |
| VAL         | MODEL FISH                  |
| VAL         | PATHS CONTROL               |
| VAL         | PATIENT SISTER              |
| VAL         | PREJUDICE OLEANDER          |
| VAL         | PRIMARY GLASS               |
| VAL         | SHAWSHANK BUBBLE            |
| VAL         | STALLION SUNDANCE           |
| VAL         | STAMPEDE DISTURBING         |
| VAL         | STRANGER STRANGERS          |
| VAL         | TOWN ARK                    |
| VAL         | UNITED PILOT                |
| VAL         | WATCH TRACY                 |
| VAL         | WEDDING APOLLO              |
| VAL         | WORKING MICROCOSMOS         |
| VAL         | YOUTH KICK                  |
| TOM         | ANALYZE HOOSIERS            |
| TOM         | CADDYSHACK JEDI             |
| TOM         | CLUB GRAFFITI               |
| TOM         | CONGENIALITY QUEST          |
| TOM         | DESIRE ALIEN                |
| TOM         | DONNIE ALLEY                |
| TOM         | EGG IGBY                    |
| TOM         | FREEDOM CLEOPATRA           |
| TOM         | FRISCO FORREST              |
| TOM         | GENTLEMEN STAGE             |
| TOM         | IDAHO LOVE                  |
| TOM         | IDOLS SNATCHERS             |
| TOM         | INDIAN LOVE                 |
| TOM         | KISSING DOLLS               |
| TOM         | LEGEND JEDI                 |
| TOM         | MAGIC MALLRATS              |
| TOM         | MISSION ZOOLANDER           |
| TOM         | NECKLACE OUTBREAK           |
| TOM         | NEIGHBORS CHARADE           |
| TOM         | PURPLE MOVIE                |
| TOM         | SHRUNK DIVINE               |
| TOM         | SPICE SORORITY              |
| TOM         | STALLION SUNDANCE           |
| TOM         | STRANGER STRANGERS          |
| TOM         | TARZAN VIDEOTAPE            |
| GOLDIE      | BILKO ANONYMOUS             |
| GOLDIE      | BINGO TALENTED              |
| GOLDIE      | COMANCHEROS ENEMY           |
| GOLDIE      | DAISY MENAGERIE             |
| GOLDIE      | DESERT POSEIDON             |
| GOLDIE      | EVERYONE CRAFT              |
| GOLDIE      | EXORCIST STING              |
| GOLDIE      | FLAMINGOS CONNECTICUT       |
| GOLDIE      | HIGH ENCINO                 |
| GOLDIE      | HOLY TADPOLE                |
| GOLDIE      | HOOSIERS BIRDCAGE           |
| GOLDIE      | INCH JET                    |
| GOLDIE      | JASON TRAP                  |
| GOLDIE      | MARRIED GO                  |
| GOLDIE      | MOD SECRETARY               |
| GOLDIE      | MOSQUITO ARMAGEDDON         |
| GOLDIE      | MUMMY CREATURES             |
| GOLDIE      | OUTLAW HANKY                |
| GOLDIE      | PITY BOUND                  |
| GOLDIE      | POLLOCK DELIVERANCE         |
| GOLDIE      | PRIDE ALAMO                 |
| GOLDIE      | PRIX UNDEFEATED             |
| GOLDIE      | PUNK DIVORCE                |
| GOLDIE      | ROBBERY BRIGHT              |
| GOLDIE      | SEA VIRGIN                  |
| GOLDIE      | SNATCHERS MONTEZUMA         |
| GOLDIE      | SPIRITED CASUALTIES         |
| GOLDIE      | UNBREAKABLE KARATE          |
| JOHNNY      | ACADEMY DINOSAUR            |
| JOHNNY      | ALAMO VIDEOTAPE             |
| JOHNNY      | ARABIA DOGMA                |
| JOHNNY      | BUNCH MINDS                 |
| JOHNNY      | CATCH AMISTAD               |
| JOHNNY      | CLYDE THEORY                |
| JOHNNY      | CONNECTICUT TRAMP           |
| JOHNNY      | DESIRE ALIEN                |
| JOHNNY      | DISCIPLE MOTHER             |
| JOHNNY      | FLYING HOOK                 |
| JOHNNY      | GRAFFITI LOVE               |
| JOHNNY      | HAMLET WISDOM               |
| JOHNNY      | HANGING DEEP                |
| JOHNNY      | INSTINCT AIRPORT            |
| JOHNNY      | INTOLERABLE INTENTIONS      |
| JOHNNY      | KARATE MOON                 |
| JOHNNY      | LIES TREATMENT              |
| JOHNNY      | REIGN GENTLEMEN             |
| JOHNNY      | ROCK INSTINCT               |
| JOHNNY      | ROOTS REMEMBER              |
| JOHNNY      | ROXANNE REBEL               |
| JOHNNY      | RUSHMORE MERMAID            |
| JOHNNY      | SIMON NORTH                 |
| JOHNNY      | SPY MILE                    |
| JOHNNY      | SUPERFLY TRIP               |
| JOHNNY      | SUSPECTS QUILLS             |
| JOHNNY      | THIEF PELICAN               |
| JOHNNY      | VAMPIRE WHALE               |
| JOHNNY      | VELVET TERMINATOR           |
| JODIE       | AFFAIR PREJUDICE            |
| JODIE       | BEAST HUNCHBACK             |
| JODIE       | BEVERLY OUTLAW              |
| JODIE       | BOOGIE AMELIE               |
| JODIE       | BROOKLYN DESERT             |
| JODIE       | CIDER DESIRE                |
| JODIE       | CLOSER BANG                 |
| JODIE       | CROW GREASE                 |
| JODIE       | DAISY MENAGERIE             |
| JODIE       | DARN FORRESTER              |
| JODIE       | DIARY PANIC                 |
| JODIE       | DRACULA CRYSTAL             |
| JODIE       | DREAM PICKUP                |
| JODIE       | FATAL HAUNTED               |
| JODIE       | FRENCH HOLIDAY              |
| JODIE       | GROOVE FICTION              |
| JODIE       | MADISON TRAP                |
| JODIE       | MOONSHINE CABIN             |
| JODIE       | PARADISE SABRINA            |
| JODIE       | PET HAUNTING                |
| JODIE       | PICKUP DRIVING              |
| JODIE       | REDS POCUS                  |
| JODIE       | REMEMBER DIARY              |
| JODIE       | SENSE GREEK                 |
| JODIE       | SHANGHAI TYCOON             |
| JODIE       | SIMON NORTH                 |
| JODIE       | TOMATOES HELLFIGHTERS       |
| JODIE       | TROJAN TOMORROW             |
| JODIE       | VIETNAM SMOOCHY             |
| TOM         | ANALYZE HOOSIERS            |
| TOM         | CHASING FIGHT               |
| TOM         | FEUD FROGMEN                |
| TOM         | FLAMINGOS CONNECTICUT       |
| TOM         | FREAKY POCUS                |
| TOM         | KISS GLORY                  |
| TOM         | KNOCK WARLOCK               |
| TOM         | LABYRINTH LEAGUE            |
| TOM         | LOLA AGENT                  |
| TOM         | LOVE SUICIDES               |
| TOM         | MADRE GABLES                |
| TOM         | MEMENTO ZOOLANDER           |
| TOM         | OUTLAW HANKY                |
| TOM         | PATTON INTERVIEW            |
| TOM         | PERSONAL LADYBUGS           |
| TOM         | POCUS PULP                  |
| TOM         | RAINBOW SHOCK               |
| TOM         | ROCKETEER MOTHER            |
| TOM         | SILVERADO GOLDFINGER        |
| TOM         | SUIT WALLS                  |
| TOM         | SUNRISE LEAGUE              |
| TOM         | SUPER WYOMING               |
| TOM         | TARZAN VIDEOTAPE            |
| TOM         | TIGHTS DAWN                 |
| TOM         | TRANSLATION SUMMER          |
| TOM         | UNDEFEATED DALMATIONS       |
| TOM         | VALLEY PACKER               |
| KIRK        | AMADEUS HOLY                |
| KIRK        | ARTIST COLDBLOODED          |
| KIRK        | BAREFOOT MANCHURIAN         |
| KIRK        | BORROWERS BEDAZZLED         |
| KIRK        | BULL SHAWSHANK              |
| KIRK        | CHOCOLAT HARRY              |
| KIRK        | CLUE GRAIL                  |
| KIRK        | CONSPIRACY SPIRIT           |
| KIRK        | DOGMA FAMILY                |
| KIRK        | ELEMENT FREDDY              |
| KIRK        | FORRESTER COMANCHEROS       |
| KIRK        | FURY MURDER                 |
| KIRK        | GLADIATOR WESTWARD          |
| KIRK        | GREASE YOUTH                |
| KIRK        | HEAVEN FREEDOM              |
| KIRK        | INSIDER ARIZONA             |
| KIRK        | LOST BIRD                   |
| KIRK        | MOSQUITO ARMAGEDDON         |
| KIRK        | MULHOLLAND BEAST            |
| KIRK        | MURDER ANTITRUST            |
| KIRK        | NETWORK PEAK                |
| KIRK        | RUSH GOODFELLAS             |
| KIRK        | SPICE SORORITY              |
| KIRK        | SPLENDOR PATTON             |
| KIRK        | TUXEDO MILE                 |
| KIRK        | WARDROBE PHANTOM            |
| NICK        | BEACH HEARTBREAKERS         |
| NICK        | BOILED DARES                |
| NICK        | BORN SPINAL                 |
| NICK        | BRAVEHEART HUMAN            |
| NICK        | BUTTERFLY CHOCOLAT          |
| NICK        | CONGENIALITY QUEST          |
| NICK        | DOOM DANCING                |
| NICK        | EFFECT GLADIATOR            |
| NICK        | FLATLINERS KILLER           |
| NICK        | HOLES BRANNIGAN             |
| NICK        | HORROR REIGN                |
| NICK        | JUMANJI BLADE               |
| NICK        | MONSOON CAUSE               |
| NICK        | MOSQUITO ARMAGEDDON         |
| NICK        | MULAN MOON                  |
| NICK        | PRIVATE DROP                |
| NICK        | RUNAWAY TENENBAUMS          |
| NICK        | SHANGHAI TYCOON             |
| NICK        | SPEAKEASY DATE              |
| NICK        | STRANGERS GRAFFITI          |
| NICK        | TALENTED HOMICIDE           |
| NICK        | TEEN APOLLO                 |
| NICK        | TEQUILA PAST                |
| NICK        | TOOTSIE PILOT               |
| NICK        | TRADING PINOCCHIO           |
| NICK        | VARSITY TRIP                |
| NICK        | VIRGIN DAISY                |
| NICK        | WAGON JAWS                  |
| NICK        | WOMEN DORADO                |
| NICK        | ZHIVAGO CORE                |
| REESE       | ALTER VICTORY               |
| REESE       | BEHAVIOR RUNAWAY            |
| REESE       | BENEATH RUSH                |
| REESE       | CAMPUS REMEMBER             |
| REESE       | CANDLES GRAPES              |
| REESE       | COAST RAINBOW               |
| REESE       | CRANES RESERVOIR            |
| REESE       | CRYSTAL BREAKING            |
| REESE       | DEEP CRUSADE                |
| REESE       | FORRESTER COMANCHEROS       |
| REESE       | HAWK CHILL                  |
| REESE       | HIGHBALL POTTER             |
| REESE       | INSTINCT AIRPORT            |
| REESE       | INTRIGUE WORST              |
| REESE       | JERK PAYCHECK               |
| REESE       | KNOCK WARLOCK               |
| REESE       | KRAMER CHOCOLATE            |
| REESE       | LAMBS CINCINATTI            |
| REESE       | LOVER TRUMAN                |
| REESE       | PINOCCHIO SIMON             |
| REESE       | RANDOM GO                   |
| REESE       | SCALAWAG DUCK               |
| REESE       | SECRETS PARADISE            |
| REESE       | SILENCE KANE                |
| REESE       | SLUMS DUCK                  |
| REESE       | TOMORROW HUSTLER            |
| REESE       | TOWN ARK                    |
| REESE       | TRACY CIDER                 |
| REESE       | UNBREAKABLE KARATE          |
| REESE       | UNITED PILOT                |
| REESE       | WILLOW TRACY                |
| REESE       | WISDOM WORKER               |
| PARKER      | ARK RIDGEMONT               |
| PARKER      | BALLOON HOMEWARD            |
| PARKER      | CONFIDENTIAL INTERVIEW      |
| PARKER      | DRIVER ANNIE                |
| PARKER      | EXPRESS LONELY              |
| PARKER      | FISH OPUS                   |
| PARKER      | HAWK CHILL                  |
| PARKER      | IDAHO LOVE                  |
| PARKER      | INCH JET                    |
| PARKER      | INSTINCT AIRPORT            |
| PARKER      | JAWS HARRY                  |
| PARKER      | LOVERBOY ATTACKS            |
| PARKER      | LUCKY FLYING                |
| PARKER      | MEET CHOCOLATE              |
| PARKER      | RIGHT CRANES                |
| PARKER      | SAVANNAH TOWN               |
| PARKER      | SCARFACE BANG               |
| PARKER      | SONS INTERVIEW              |
| PARKER      | SPINAL ROCKY                |
| PARKER      | SPIRIT FLINTSTONES          |
| PARKER      | SQUAD FISH                  |
| PARKER      | TIES HUNGER                 |
| PARKER      | WIZARD COLDBLOODED          |
| PARKER      | WORST BANGER                |
| JULIA       | ANGELS LIFE                 |
| JULIA       | ARGONAUTS TOWN              |
| JULIA       | BANG KWAI                   |
| JULIA       | BERETS AGENT                |
| JULIA       | CONEHEADS SMOOCHY           |
| JULIA       | DISCIPLE MOTHER             |
| JULIA       | EFFECT GLADIATOR            |
| JULIA       | GASLIGHT CRUSADE            |
| JULIA       | GROUNDHOG UNCUT             |
| JULIA       | JERK PAYCHECK               |
| JULIA       | LAMBS CINCINATTI            |
| JULIA       | MIGHTY LUCK                 |
| JULIA       | PELICAN COMFORTS            |
| JULIA       | ROAD ROXANNE                |
| JULIA       | ROCK INSTINCT               |
| JULIA       | SCISSORHANDS SLUMS          |
| JULIA       | SECRETARY ROUGE             |
| JULIA       | SHINING ROSES               |
| JULIA       | SHOOTIST SUPERFLY           |
| JULIA       | TROOPERS METAL              |
| JULIA       | UNFAITHFUL KILL             |
| JULIA       | UNFORGIVEN ZOOLANDER        |
| JULIA       | VIRGIN DAISY                |
| JULIA       | WIFE TURN                   |
| FRANCES     | BRINGING HYSTERICAL         |
| FRANCES     | BROTHERHOOD BLANKET         |
| FRANCES     | CHAMPION FLATLINERS         |
| FRANCES     | CIDER DESIRE                |
| FRANCES     | COAST RAINBOW               |
| FRANCES     | DARLING BREAKING            |
| FRANCES     | DOUBLE WRATH                |
| FRANCES     | EAGLES PANKY                |
| FRANCES     | ENTRAPMENT SATISFACTION     |
| FRANCES     | EXPENDABLE STALLION         |
| FRANCES     | FIDDLER LOST                |
| FRANCES     | FINDING ANACONDA            |
| FRANCES     | GABLES METROPOLIS           |
| FRANCES     | GANGS PRIDE                 |
| FRANCES     | HOMICIDE PEACH              |
| FRANCES     | LADY STAGE                  |
| FRANCES     | MADNESS ATTACKS             |
| FRANCES     | MARRIED GO                  |
| FRANCES     | MERMAID INSECTS             |
| FRANCES     | MOTHER OLEANDER             |
| FRANCES     | OTHERS SOUP                 |
| FRANCES     | PURPLE MOVIE                |
| FRANCES     | SAGEBRUSH CLUELESS          |
| FRANCES     | SHREK LICENSE               |
| FRANCES     | UNDEFEATED DALMATIONS       |
| FRANCES     | UNTOUCHABLES SUNRISE        |
| ANNE        | APACHE DIVINE               |
| ANNE        | CINCINATTI WHISPERER        |
| ANNE        | CROWDS TELEMARK             |
| ANNE        | DANGEROUS UPTOWN            |
| ANNE        | DRAGON SQUAD                |
| ANNE        | ENCOUNTERS CURTAIN          |
| ANNE        | GANDHI KWAI                 |
| ANNE        | HALF OUTFIELD               |
| ANNE        | HARDLY ROBBERS              |
| ANNE        | HAWK CHILL                  |
| ANNE        | HOLLYWOOD ANONYMOUS         |
| ANNE        | HORN WORKING                |
| ANNE        | IRON MOON                   |
| ANNE        | LADY STAGE                  |
| ANNE        | LUST LOCK                   |
| ANNE        | MANNEQUIN WORST             |
| ANNE        | MINDS TRUMAN                |
| ANNE        | MOON BUNCH                  |
| ANNE        | PATHS CONTROL               |
| ANNE        | RACER EGG                   |
| ANNE        | REAP UNFAITHFUL             |
| ANNE        | REQUIEM TYCOON              |
| ANNE        | RIDER CADDYSHACK            |
| ANNE        | SMILE EARRING               |
| ANNE        | UPRISING UPTOWN             |
| ANNE        | WINDOW SIDE                 |
| ANNE        | WIZARD COLDBLOODED          |
| NATALIE     | CADDYSHACK JEDI             |
| NATALIE     | CONNECTION MICROCOSMOS      |
| NATALIE     | DOORS PRESIDENT             |
| NATALIE     | DOZEN LION                  |
| NATALIE     | EGG IGBY                    |
| NATALIE     | ESCAPE METROPOLIS           |
| NATALIE     | FANTASY TROOPERS            |
| NATALIE     | FEATHERS METAL              |
| NATALIE     | FOOL MOCKINGBIRD            |
| NATALIE     | GRACELAND DYNAMITE          |
| NATALIE     | HAROLD FRENCH               |
| NATALIE     | HILLS NEIGHBORS             |
| NATALIE     | HOLES BRANNIGAN             |
| NATALIE     | HOUSE DYNAMITE              |
| NATALIE     | JASON TRAP                  |
| NATALIE     | KWAI HOMEWARD               |
| NATALIE     | LICENSE WEEKEND             |
| NATALIE     | MAJESTIC FLOATS             |
| NATALIE     | MONSOON CAUSE               |
| NATALIE     | NETWORK PEAK                |
| NATALIE     | NUTS TIES                   |
| NATALIE     | OTHERS SOUP                 |
| NATALIE     | PERFECT GROOVE              |
| NATALIE     | REAR TRADING                |
| NATALIE     | RINGS HEARTBREAKERS         |
| NATALIE     | SIEGE MADRE                 |
| NATALIE     | SPINAL ROCKY                |
| NATALIE     | STAMPEDE DISTURBING         |
| NATALIE     | TORQUE BOUND                |
| NATALIE     | TWISTED PIRATES             |
| NATALIE     | UNFORGIVEN ZOOLANDER        |
| NATALIE     | WAR NOTTING                 |
| GARY        | AFRICAN EGG                 |
| GARY        | BEDAZZLED MARRIED           |
| GARY        | BUCKET BROTHERHOOD          |
| GARY        | CALENDAR GUNFIGHT           |
| GARY        | CAROL TEXAS                 |
| GARY        | CITIZEN SHREK               |
| GARY        | HANDICAP BOONDOCK           |
| GARY        | HEAD STRANGER               |
| GARY        | HOLES BRANNIGAN             |
| GARY        | INSECTS STONE               |
| GARY        | JUMANJI BLADE               |
| GARY        | LOATHING LEGALLY            |
| GARY        | NORTH TEQUILA               |
| GARY        | PICKUP DRIVING              |
| GARY        | RIVER OUTLAW                |
| GARY        | ROAD ROXANNE                |
| GARY        | ROCK INSTINCT               |
| GARY        | RUN PACIFIC                 |
| GARY        | STOCK GLASS                 |
| GARY        | TIMBERLAND SKY              |
| GARY        | TOMORROW HUSTLER            |
| GARY        | VICTORY ACADEMY             |
| GARY        | WILD APOLLO                 |
| GARY        | WORLD LEATHERNECKS          |
| GARY        | WRONG BEHAVIOR              |
| CARMEN      | AMELIE HELLFIGHTERS         |
| CARMEN      | BOWFINGER GABLES            |
| CARMEN      | BREAKING HOME               |
| CARMEN      | BUTCH PANTHER               |
| CARMEN      | DAISY MENAGERIE             |
| CARMEN      | DRACULA CRYSTAL             |
| CARMEN      | FROST HEAD                  |
| CARMEN      | GRAPES FURY                 |
| CARMEN      | GUNFIGHT MOON               |
| CARMEN      | HAWK CHILL                  |
| CARMEN      | HOLOCAUST HIGHBALL          |
| CARMEN      | JADE BUNCH                  |
| CARMEN      | LEGALLY SECRETARY           |
| CARMEN      | LESSON CLEOPATRA            |
| CARMEN      | MIXED DOORS                 |
| CARMEN      | MOONSHINE CABIN             |
| CARMEN      | PATRIOT ROMAN               |
| CARMEN      | PHANTOM GLORY               |
| CARMEN      | POLLOCK DELIVERANCE         |
| CARMEN      | RANDOM GO                   |
| CARMEN      | SMOKING BARBARELLA          |
| CARMEN      | TEEN APOLLO                 |
| CARMEN      | TELEGRAPH VOYAGE            |
| CARMEN      | TRUMAN CRAZY                |
| CARMEN      | VOYAGE LEGALLY              |
| CARMEN      | ZOOLANDER FICTION           |
| MENA        | ACADEMY DINOSAUR            |
| MENA        | ALABAMA DEVIL               |
| MENA        | BALLOON HOMEWARD            |
| MENA        | BEACH HEARTBREAKERS         |
| MENA        | BUTTERFLY CHOCOLAT          |
| MENA        | CARRIE BUNCH                |
| MENA        | CASUALTIES ENCINO           |
| MENA        | CONTACT ANONYMOUS           |
| MENA        | DROP WATERFRONT             |
| MENA        | EARLY HOME                  |
| MENA        | ENGLISH BULWORTH            |
| MENA        | FELLOWSHIP AUTUMN           |
| MENA        | GILMORE BOILED              |
| MENA        | GUMP DATE                   |
| MENA        | ICE CROSSING                |
| MENA        | INTERVIEW LIAISONS          |
| MENA        | JUMANJI BLADE               |
| MENA        | JUNGLE CLOSER               |
| MENA        | LAMBS CINCINATTI            |
| MENA        | LIAISONS SWEET              |
| MENA        | MICROCOSMOS PARADISE        |
| MENA        | MIGHTY LUCK                 |
| MENA        | MILE MULAN                  |
| MENA        | PRIMARY GLASS               |
| MENA        | REQUIEM TYCOON              |
| MENA        | RESURRECTION SILVERADO      |
| MENA        | VARSITY TRIP                |
| MENA        | VISION TORQUE               |
| MENA        | WASH HEAVENLY               |
| MENA        | WIZARD COLDBLOODED          |
| PENELOPE    | BOILED DARES                |
| PENELOPE    | CAUSE DATE                  |
| PENELOPE    | CIDER DESIRE                |
| PENELOPE    | CORE SUIT                   |
| PENELOPE    | ENGLISH BULWORTH            |
| PENELOPE    | EXCITEMENT EVE              |
| PENELOPE    | FAMILY SWEET                |
| PENELOPE    | GANDHI KWAI                 |
| PENELOPE    | JUGGLER HARDLY              |
| PENELOPE    | LAWLESS VISION              |
| PENELOPE    | LION UNCUT                  |
| PENELOPE    | MADRE GABLES                |
| PENELOPE    | MOTIONS DETAILS             |
| PENELOPE    | OLEANDER CLUE               |
| PENELOPE    | OZ LIAISONS                 |
| PENELOPE    | PARIS WEEKEND               |
| PENELOPE    | RUSHMORE MERMAID            |
| PENELOPE    | SATURDAY LAMBS              |
| PENELOPE    | STATE WASTELAND             |
| PENELOPE    | SUBMARINE BED               |
| PENELOPE    | SUIT WALLS                  |
| PENELOPE    | TROOPERS METAL              |
| PENELOPE    | WESTWARD SEABISCUIT         |
| PENELOPE    | WORKER TARZAN               |
| PENELOPE    | WORLD LEATHERNECKS          |
| FAY         | AIRPORT POLLOCK             |
| FAY         | ANONYMOUS HUMAN             |
| FAY         | BIRD INDEPENDENCE           |
| FAY         | CRUSADE HONEY               |
| FAY         | FELLOWSHIP AUTUMN           |
| FAY         | FLAMINGOS CONNECTICUT       |
| FAY         | FRONTIER CABIN              |
| FAY         | HARRY IDAHO                 |
| FAY         | JERSEY SASSY                |
| FAY         | JET NEIGHBORS               |
| FAY         | MOVIE SHAKESPEARE           |
| FAY         | MUSSOLINI SPOILERS          |
| FAY         | NEMO CAMPUS                 |
| FAY         | RACER EGG                   |
| FAY         | SECRET GROUNDHOG            |
| FAY         | SHOOTIST SUPERFLY           |
| FAY         | SNATCHERS MONTEZUMA         |
| FAY         | SPICE SORORITY              |
| FAY         | VACATION BOONDOCK           |
| FAY         | WATCH TRACY                 |
| DAN         | BEDAZZLED MARRIED           |
| DAN         | BOONDOCK BALLROOM           |
| DAN         | DESTINY SATURDAY            |
| DAN         | DIVINE RESURRECTION         |
| DAN         | EYES DRIVING                |
| DAN         | FELLOWSHIP AUTUMN           |
| DAN         | GHOST GROUNDHOG             |
| DAN         | GROOVE FICTION              |
| DAN         | HILLS NEIGHBORS             |
| DAN         | HOLIDAY GAMES               |
| DAN         | INDEPENDENCE HOTEL          |
| DAN         | INSIDER ARIZONA             |
| DAN         | JADE BUNCH                  |
| DAN         | LIES TREATMENT              |
| DAN         | MONTEREY LABYRINTH          |
| DAN         | REUNION WITCHES             |
| DAN         | RUN PACIFIC                 |
| DAN         | SCHOOL JACKET               |
| DAN         | SEVEN SWARM                 |
| DAN         | SIEGE MADRE                 |
| DAN         | STEERS ARMAGEDDON           |
| DAN         | STRAIGHT HOURS              |
| DAN         | SUMMER SCARFACE             |
| DAN         | SUPERFLY TRIP               |
| DAN         | TITANIC BOONDOCK            |
| DAN         | TITANS JERK                 |
| DAN         | VANISHING ROCKY             |
| DAN         | WATERSHIP FRONTIER          |
| JUDE        | ALLEY EVOLUTION             |
| JUDE        | ARABIA DOGMA                |
| JUDE        | BROTHERHOOD BLANKET         |
| JUDE        | CAMELOT VACATION            |
| JUDE        | CARRIE BUNCH                |
| JUDE        | CHAMPION FLATLINERS         |
| JUDE        | CHINATOWN GLADIATOR         |
| JUDE        | CITIZEN SHREK               |
| JUDE        | CROSSING DIVORCE            |
| JUDE        | DATE SPEED                  |
| JUDE        | DRUMS DYNAMITE              |
| JUDE        | EAGLES PANKY                |
| JUDE        | FIREBALL PHILADELPHIA       |
| JUDE        | FRONTIER CABIN              |
| JUDE        | HALLOWEEN NUTS              |
| JUDE        | HOUSE DYNAMITE              |
| JUDE        | ICE CROSSING                |
| JUDE        | KNOCK WARLOCK               |
| JUDE        | MONSTER SPARTACUS           |
| JUDE        | MULHOLLAND BEAST            |
| JUDE        | OPEN AFRICAN                |
| JUDE        | PLATOON INSTINCT            |
| JUDE        | QUEST MUSSOLINI             |
| JUDE        | RANDOM GO                   |
| JUDE        | REAR TRADING                |
| JUDE        | ROCK INSTINCT               |
| JUDE        | SCALAWAG DUCK               |
| JUDE        | STRANGELOVE DESIRE          |
| JUDE        | TIMBERLAND SKY              |
| JUDE        | TWISTED PIRATES             |
| CHRISTIAN   | BACKLASH UNDEFEATED         |
| CHRISTIAN   | BETRAYED REAR               |
| CHRISTIAN   | CAPER MOTIONS               |
| CHRISTIAN   | CATCH AMISTAD               |
| CHRISTIAN   | CHANCE RESURRECTION         |
| CHRISTIAN   | CONFUSED CANDLES            |
| CHRISTIAN   | CUPBOARD SINNERS            |
| CHRISTIAN   | DIVIDE MONSTER              |
| CHRISTIAN   | DOOM DANCING                |
| CHRISTIAN   | DOORS PRESIDENT             |
| CHRISTIAN   | DRIVER ANNIE                |
| CHRISTIAN   | FEATHERS METAL              |
| CHRISTIAN   | FIRE WOLVES                 |
| CHRISTIAN   | HILLS NEIGHBORS             |
| CHRISTIAN   | HOME PITY                   |
| CHRISTIAN   | INNOCENT USUAL              |
| CHRISTIAN   | JAWBREAKER BROOKLYN         |
| CHRISTIAN   | LUKE MUMMY                  |
| CHRISTIAN   | MAGNOLIA FORRESTER          |
| CHRISTIAN   | MAIDEN HOME                 |
| CHRISTIAN   | MAKER GABLES                |
| CHRISTIAN   | MILLION ACE                 |
| CHRISTIAN   | MOURNING PURPLE             |
| CHRISTIAN   | NUTS TIES                   |
| CHRISTIAN   | OKLAHOMA JUMANJI            |
| CHRISTIAN   | OPERATION OPERATION         |
| CHRISTIAN   | PRINCESS GIANT              |
| CHRISTIAN   | RESERVOIR ADAPTATION        |
| CHRISTIAN   | SABRINA MIDNIGHT            |
| CHRISTIAN   | SINNERS ATLANTIS            |
| CHRISTIAN   | STREETCAR INTENTIONS        |
| CHRISTIAN   | SUBMARINE BED               |
| DUSTIN      | AFRICAN EGG                 |
| DUSTIN      | AUTUMN CROW                 |
| DUSTIN      | BANGER PINOCCHIO            |
| DUSTIN      | BILL OTHERS                 |
| DUSTIN      | BORN SPINAL                 |
| DUSTIN      | CAROL TEXAS                 |
| DUSTIN      | CAUSE DATE                  |
| DUSTIN      | CELEBRITY HORN              |
| DUSTIN      | CONVERSATION DOWNHILL       |
| DUSTIN      | DARKO DORADO                |
| DUSTIN      | DONNIE ALLEY                |
| DUSTIN      | EXPENDABLE STALLION         |
| DUSTIN      | HOBBIT ALIEN                |
| DUSTIN      | METROPOLIS COMA             |
| DUSTIN      | OSCAR GOLD                  |
| DUSTIN      | PACIFIC AMISTAD             |
| DUSTIN      | POLLOCK DELIVERANCE         |
| DUSTIN      | PREJUDICE OLEANDER          |
| DUSTIN      | PULP BEVERLY                |
| DUSTIN      | RAINBOW SHOCK               |
| DUSTIN      | RULES HUMAN                 |
| DUSTIN      | SEA VIRGIN                  |
| DUSTIN      | STRANGER STRANGERS          |
| DUSTIN      | SUMMER SCARFACE             |
| DUSTIN      | VILLAIN DESPERATE           |
| DUSTIN      | VIRTUAL SPOILERS            |
| DUSTIN      | WONDERFUL DROP              |
| HENRY       | APACHE DIVINE               |
| HENRY       | BONNIE HOLOCAUST            |
| HENRY       | CHAMBER ITALIAN             |
| HENRY       | CHICKEN HELLFIGHTERS        |
| HENRY       | CONNECTICUT TRAMP           |
| HENRY       | CONQUERER NUTS              |
| HENRY       | CRAFT OUTFIELD              |
| HENRY       | DESERT POSEIDON             |
| HENRY       | DIVIDE MONSTER              |
| HENRY       | DOGMA FAMILY                |
| HENRY       | DRIFTER COMMANDMENTS        |
| HENRY       | DUMBO LUST                  |
| HENRY       | EXTRAORDINARY CONQUERER     |
| HENRY       | FACTORY DRAGON              |
| HENRY       | FREDDY STORM                |
| HENRY       | GRAPES FURY                 |
| HENRY       | HOLLYWOOD ANONYMOUS         |
| HENRY       | HOURS RAGE                  |
| HENRY       | KANE EXORCIST               |
| HENRY       | LOUISIANA HARRY             |
| HENRY       | MAIDEN HOME                 |
| HENRY       | PARIS WEEKEND               |
| HENRY       | PATTON INTERVIEW            |
| HENRY       | PILOT HOOSIERS              |
| HENRY       | RUSHMORE MERMAID            |
| HENRY       | SCORPION APOLLO             |
| HENRY       | SHANE DARKNESS              |
| HENRY       | SHANGHAI TYCOON             |
| HENRY       | SLEEPLESS MONSOON           |
| HENRY       | SPIRIT FLINTSTONES          |
| HENRY       | SPY MILE                    |
| HENRY       | UPTOWN YOUNG                |
| HENRY       | WAGON JAWS                  |
| HENRY       | WHALE BIKINI                |
| HENRY       | WONKA SEA                   |
| CHRISTIAN   | DIVIDE MONSTER              |
| CHRISTIAN   | DIVORCE SHINING             |
| CHRISTIAN   | FELLOWSHIP AUTUMN           |
| CHRISTIAN   | GLORY TRACY                 |
| CHRISTIAN   | GRACELAND DYNAMITE          |
| CHRISTIAN   | GRAFFITI LOVE               |
| CHRISTIAN   | HOLLYWOOD ANONYMOUS         |
| CHRISTIAN   | HORN WORKING                |
| CHRISTIAN   | LAMBS CINCINATTI            |
| CHRISTIAN   | LIAISONS SWEET              |
| CHRISTIAN   | LIBERTY MAGNIFICENT         |
| CHRISTIAN   | LOVE SUICIDES               |
| CHRISTIAN   | LOVER TRUMAN                |
| CHRISTIAN   | MOB DUFFEL                  |
| CHRISTIAN   | OPPOSITE NECKLACE           |
| CHRISTIAN   | OUTLAW HANKY                |
| CHRISTIAN   | OZ LIAISONS                 |
| CHRISTIAN   | PUNK DIVORCE                |
| CHRISTIAN   | RUNNER MADIGAN              |
| CHRISTIAN   | SAVANNAH TOWN               |
| CHRISTIAN   | SCALAWAG DUCK               |
| CHRISTIAN   | SENSIBILITY REAR            |
| CHRISTIAN   | SPIRITED CASUALTIES         |
| CHRISTIAN   | SPLASH GUMP                 |
| CHRISTIAN   | WORLD LEATHERNECKS          |
| JAYNE       | AGENT TRUMAN                |
| JAYNE       | ARTIST COLDBLOODED          |
| JAYNE       | BANGER PINOCCHIO            |
| JAYNE       | BROOKLYN DESERT             |
| JAYNE       | BROTHERHOOD BLANKET         |
| JAYNE       | CAUSE DATE                  |
| JAYNE       | CRYSTAL BREAKING            |
| JAYNE       | DARLING BREAKING            |
| JAYNE       | DINOSAUR SECRETARY          |
| JAYNE       | EDGE KISSING                |
| JAYNE       | EXPENDABLE STALLION         |
| JAYNE       | FRIDA SLIPPER               |
| JAYNE       | GRAIL FRANKENSTEIN          |
| JAYNE       | GROUNDHOG UNCUT             |
| JAYNE       | HALLOWEEN NUTS              |
| JAYNE       | HANOVER GALAXY              |
| JAYNE       | HAUNTING PIANIST            |
| JAYNE       | HEDWIG ALTER                |
| JAYNE       | HOMICIDE PEACH              |
| JAYNE       | HYDE DOCTOR                 |
| JAYNE       | INDEPENDENCE HOTEL          |
| JAYNE       | INTERVIEW LIAISONS          |
| JAYNE       | POLISH BROOKLYN             |
| JAYNE       | QUEST MUSSOLINI             |
| JAYNE       | RECORDS ZORRO               |
| JAYNE       | VOYAGE LEGALLY              |
| JAYNE       | WOLVES DESIRE               |
| JAYNE       | WORKER TARZAN               |
| JAYNE       | WORLD LEATHERNECKS          |
| CAMERON     | BINGO TALENTED              |
| CAMERON     | CHAMPION FLATLINERS         |
| CAMERON     | COMA HEAD                   |
| CAMERON     | DARES PLUTO                 |
| CAMERON     | DESTINATION JERK            |
| CAMERON     | DOZEN LION                  |
| CAMERON     | DRACULA CRYSTAL             |
| CAMERON     | ELF MURDER                  |
| CAMERON     | HALL CASSIDY                |
| CAMERON     | LESSON CLEOPATRA            |
| CAMERON     | OCTOBER SUBMARINE           |
| CAMERON     | SATISFACTION CONFIDENTIAL   |
| CAMERON     | SEVEN SWARM                 |
| CAMERON     | SLIPPER FIDELITY            |
| CAMERON     | TITANS JERK                 |
| CAMERON     | VALLEY PACKER               |
| CAMERON     | VIRGIN DAISY                |
| CAMERON     | VIRGINIAN PLUTO             |
| CAMERON     | WOLVES DESIRE               |
| RAY         | ADAPTATION HOLES            |
| RAY         | ALADDIN CALENDAR            |
| RAY         | ARIZONA BANG                |
| RAY         | BOONDOCK BALLROOM           |
| RAY         | BORN SPINAL                 |
| RAY         | CASPER DRAGONFLY            |
| RAY         | CRUSADE HONEY               |
| RAY         | EMPIRE MALKOVICH            |
| RAY         | EVOLUTION ALTER             |
| RAY         | FELLOWSHIP AUTUMN           |
| RAY         | FREEDOM CLEOPATRA           |
| RAY         | GABLES METROPOLIS           |
| RAY         | IDAHO LOVE                  |
| RAY         | IRON MOON                   |
| RAY         | ISLAND EXORCIST             |
| RAY         | LADY STAGE                  |
| RAY         | MADIGAN DORADO              |
| RAY         | MANCHURIAN CURTAIN          |
| RAY         | MENAGERIE RUSHMORE          |
| RAY         | METROPOLIS COMA             |
| RAY         | MOONWALKER FOOL             |
| RAY         | NATIONAL STORY              |
| RAY         | OUTBREAK DIVINE             |
| RAY         | PREJUDICE OLEANDER          |
| RAY         | SPLASH GUMP                 |
| RAY         | STRANGELOVE DESIRE          |
| RAY         | SUICIDES SILENCE            |
| RAY         | UNCUT SUICIDES              |
| RAY         | UNITED PILOT                |
| RAY         | WIZARD COLDBLOODED          |
| ANGELA      | ARMAGEDDON LOST             |
| ANGELA      | AUTUMN CROW                 |
| ANGELA      | BRIDE INTRIGUE              |
| ANGELA      | BULWORTH COMMANDMENTS       |
| ANGELA      | CANDLES GRAPES              |
| ANGELA      | CASSIDY WYOMING             |
| ANGELA      | CLONES PINOCCHIO            |
| ANGELA      | ELEMENT FREDDY              |
| ANGELA      | FATAL HAUNTED               |
| ANGELA      | FRISCO FORREST              |
| ANGELA      | GAMES BOWFINGER             |
| ANGELA      | GOSFORD DONNIE              |
| ANGELA      | HANOVER GALAXY              |
| ANGELA      | ISLAND EXORCIST             |
| ANGELA      | JAPANESE RUN                |
| ANGELA      | JASON TRAP                  |
| ANGELA      | JUMPING WRATH               |
| ANGELA      | KICK SAVANNAH               |
| ANGELA      | LEGEND JEDI                 |
| ANGELA      | LESSON CLEOPATRA            |
| ANGELA      | LUKE MUMMY                  |
| ANGELA      | MALTESE HOPE                |
| ANGELA      | METAL ARMAGEDDON            |
| ANGELA      | MILE MULAN                  |
| ANGELA      | NASH CHOCOLAT               |
| ANGELA      | PARIS WEEKEND               |
| ANGELA      | PITY BOUND                  |
| ANGELA      | PREJUDICE OLEANDER          |
| ANGELA      | RANDOM GO                   |
| ANGELA      | ROBBERS JOON                |
| ANGELA      | STRANGELOVE DESIRE          |
| ANGELA      | VELVET TERMINATOR           |
| ANGELA      | VOYAGE LEGALLY              |
| ANGELA      | WATERSHIP FRONTIER          |
| MARY        | BARBARELLA STREETCAR        |
| MARY        | CHILL LUCK                  |
| MARY        | DANGEROUS UPTOWN            |
| MARY        | DESTINY SATURDAY            |
| MARY        | DEVIL DESIRE                |
| MARY        | DIARY PANIC                 |
| MARY        | ENDING CROWDS               |
| MARY        | FALCON VOLUME               |
| MARY        | FUGITIVE MAGUIRE            |
| MARY        | GARDEN ISLAND               |
| MARY        | GLEAMING JAWBREAKER         |
| MARY        | GRAPES FURY                 |
| MARY        | HOLOCAUST HIGHBALL          |
| MARY        | HORROR REIGN                |
| MARY        | MAKER GABLES                |
| MARY        | MURDER ANTITRUST            |
| MARY        | PHILADELPHIA WIFE           |
| MARY        | PRIMARY GLASS               |
| MARY        | QUEEN LUKE                  |
| MARY        | REQUIEM TYCOON              |
| MARY        | SCHOOL JACKET               |
| MARY        | SHRUNK DIVINE               |
| MARY        | SPINAL ROCKY                |
| MARY        | SWEDEN SHINING              |
| MARY        | TREASURE COMMAND            |
| MARY        | TRUMAN CRAZY                |
| MARY        | UPTOWN YOUNG                |
| MARY        | VOYAGE LEGALLY              |
| MARY        | WAR NOTTING                 |
| MARY        | WARS PLUTO                  |
| MARY        | ZOOLANDER FICTION           |
| JESSICA     | ANALYZE HOOSIERS            |
| JESSICA     | BASIC EASY                  |
| JESSICA     | BERETS AGENT                |
| JESSICA     | CHINATOWN GLADIATOR         |
| JESSICA     | DOOM DANCING                |
| JESSICA     | DORADO NOTTING              |
| JESSICA     | DROP WATERFRONT             |
| JESSICA     | HEAD STRANGER               |
| JESSICA     | JAWBREAKER BROOKLYN         |
| JESSICA     | KICK SAVANNAH               |
| JESSICA     | LEAGUE HELLFIGHTERS         |
| JESSICA     | MIGHTY LUCK                 |
| JESSICA     | MOULIN WAKE                 |
| JESSICA     | REQUIEM TYCOON              |
| JESSICA     | RESERVOIR ADAPTATION        |
| JESSICA     | RIGHT CRANES                |
| JESSICA     | SAVANNAH TOWN               |
| JESSICA     | SUIT WALLS                  |
| JESSICA     | SWARM GOLD                  |
| JESSICA     | TRUMAN CRAZY                |
| JESSICA     | VIRGINIAN PLUTO             |
| JESSICA     | WHISPERER GIANT             |
| JESSICA     | WOLVES DESIRE               |
| RIP         | ALABAMA DEVIL               |
| RIP         | ATTRACTION NEWTON           |
| RIP         | CHAMBER ITALIAN             |
| RIP         | CLUE GRAIL                  |
| RIP         | DANCES NONE                 |
| RIP         | DATE SPEED                  |
| RIP         | DAWN POND                   |
| RIP         | DRIVING POLISH              |
| RIP         | EXPRESS LONELY              |
| RIP         | FINDING ANACONDA            |
| RIP         | FLOATS GARDEN               |
| RIP         | FORWARD TEMPLE              |
| RIP         | GAMES BOWFINGER             |
| RIP         | GILBERT PELICAN             |
| RIP         | GREATEST NORTH              |
| RIP         | GREEK EVERYONE              |
| RIP         | GUMP DATE                   |
| RIP         | HANGING DEEP                |
| RIP         | HOTEL HAPPINESS             |
| RIP         | KILL BROTHERHOOD            |
| RIP         | MUPPET MILE                 |
| RIP         | PANKY SUBMARINE             |
| RIP         | PATTON INTERVIEW            |
| RIP         | PERDITION FARGO             |
| RIP         | QUEEN LUKE                  |
| RIP         | ROXANNE REBEL               |
| RIP         | SPOILERS HELLFIGHTERS       |
| RIP         | STALLION SUNDANCE           |
| RIP         | STAMPEDE DISTURBING         |
| RIP         | WHALE BIKINI                |
| KENNETH     | ALIEN CENTER                |
| KENNETH     | BORN SPINAL                 |
| KENNETH     | CADDYSHACK JEDI             |
| KENNETH     | DADDY PITTSBURGH            |
| KENNETH     | DIVINE RESURRECTION         |
| KENNETH     | EXCITEMENT EVE              |
| KENNETH     | FALCON VOLUME               |
| KENNETH     | FEATHERS METAL              |
| KENNETH     | GRAFFITI LOVE               |
| KENNETH     | HANGING DEEP                |
| KENNETH     | ILLUSION AMELIE             |
| KENNETH     | INTOLERABLE INTENTIONS      |
| KENNETH     | LONELY ELEPHANT             |
| KENNETH     | MUSSOLINI SPOILERS          |
| KENNETH     | REDEMPTION COMFORTS         |
| KENNETH     | REEF SALUTE                 |
| KENNETH     | SANTA PARIS                 |
| KENNETH     | SHOW LORD                   |
| KENNETH     | SUNDANCE INVASION           |
| KENNETH     | TAXI KICK                   |
| KENNETH     | TROUBLE DATE                |
| MICHELLE    | BAKED CLEOPATRA             |
| MICHELLE    | BANG KWAI                   |
| MICHELLE    | BOWFINGER GABLES            |
| MICHELLE    | DADDY PITTSBURGH            |
| MICHELLE    | DETAILS PACKER              |
| MICHELLE    | DRACULA CRYSTAL             |
| MICHELLE    | EVERYONE CRAFT              |
| MICHELLE    | FARGO GANDHI                |
| MICHELLE    | FULL FLATLINERS             |
| MICHELLE    | HELLFIGHTERS SIERRA         |
| MICHELLE    | IMAGE PRINCESS              |
| MICHELLE    | INTOLERABLE INTENTIONS      |
| MICHELLE    | KWAI HOMEWARD               |
| MICHELLE    | MIXED DOORS                 |
| MICHELLE    | NORTHWEST POLISH            |
| MICHELLE    | PANKY SUBMARINE             |
| MICHELLE    | REQUIEM TYCOON              |
| MICHELLE    | SOUTH WAIT                  |
| MICHELLE    | SPOILERS HELLFIGHTERS       |
| MICHELLE    | STREETCAR INTENTIONS        |
| MICHELLE    | SUSPECTS QUILLS             |
| MICHELLE    | WAIT CIDER                  |
| MICHELLE    | WATERFRONT DELIVERANCE      |
| ADAM        | ANNIE IDENTITY              |
| ADAM        | BALLROOM MOCKINGBIRD        |
| ADAM        | DISCIPLE MOTHER             |
| ADAM        | FIREBALL PHILADELPHIA       |
| ADAM        | GLADIATOR WESTWARD          |
| ADAM        | GLORY TRACY                 |
| ADAM        | GROUNDHOG UNCUT             |
| ADAM        | HAPPINESS UNITED            |
| ADAM        | IDOLS SNATCHERS             |
| ADAM        | LOSER HUSTLER               |
| ADAM        | MARS ROMAN                  |
| ADAM        | MIDNIGHT WESTWARD           |
| ADAM        | OPERATION OPERATION         |
| ADAM        | SEABISCUIT PUNK             |
| ADAM        | SPLENDOR PATTON             |
| ADAM        | TADPOLE PARK                |
| ADAM        | TWISTED PIRATES             |
| ADAM        | WANDA CHAMBER               |
| SEAN        | ARABIA DOGMA                |
| SEAN        | CHINATOWN GLADIATOR         |
| SEAN        | DIVORCE SHINING             |
| SEAN        | DRACULA CRYSTAL             |
| SEAN        | ENOUGH RAGING               |
| SEAN        | EXPRESS LONELY              |
| SEAN        | FLOATS GARDEN               |
| SEAN        | FORWARD TEMPLE              |
| SEAN        | HAUNTED ANTITRUST           |
| SEAN        | IDOLS SNATCHERS             |
| SEAN        | MAGUIRE APACHE              |
| SEAN        | MUSCLE BRIGHT               |
| SEAN        | NEWTON LABYRINTH            |
| SEAN        | OLEANDER CLUE               |
| SEAN        | OPUS ICE                    |
| SEAN        | PATTON INTERVIEW            |
| SEAN        | REBEL AIRPORT               |
| SEAN        | ROOM ROMAN                  |
| SEAN        | SAGEBRUSH CLUELESS          |
| SEAN        | SEABISCUIT PUNK             |
| SEAN        | STRANGERS GRAFFITI          |
| SEAN        | SUNRISE LEAGUE              |
| SEAN        | VELVET TERMINATOR           |
| SEAN        | WANDA CHAMBER               |
| SEAN        | WATERFRONT DELIVERANCE      |
| SEAN        | WEST LION                   |
| GARY        | ARGONAUTS TOWN              |
| GARY        | ATTRACTION NEWTON           |
| GARY        | BALLOON HOMEWARD            |
| GARY        | BIRDS PERDITION             |
| GARY        | CHOCOLATE DUCK              |
| GARY        | DOUBLE WRATH                |
| GARY        | EGYPT TENENBAUMS            |
| GARY        | FLATLINERS KILLER           |
| GARY        | GRAFFITI LOVE               |
| GARY        | GREEDY ROOTS                |
| GARY        | INTRIGUE WORST              |
| GARY        | MAGNIFICENT CHITTY          |
| GARY        | MASK PEACH                  |
| GARY        | MASKED BUBBLE               |
| GARY        | MATRIX SNOWMAN              |
| GARY        | NORTH TEQUILA               |
| GARY        | PAYCHECK WAIT               |
| GARY        | PEACH INNOCENT              |
| GARY        | QUEST MUSSOLINI             |
| GARY        | RUGRATS SHAKESPEARE         |
| GARY        | SEA VIRGIN                  |
| GARY        | SOUTH WAIT                  |
| GARY        | VANISHING ROCKY             |
| GARY        | VIRTUAL SPOILERS            |
| GARY        | VOLUME HOUSE                |
| GARY        | ZHIVAGO CORE                |
| MILLA       | ANTHEM LUKE                 |
| MILLA       | ATTACKS HATE                |
| MILLA       | CANDLES GRAPES              |
| MILLA       | COWBOY DOOM                 |
| MILLA       | CROSSING DIVORCE            |
| MILLA       | DAISY MENAGERIE             |
| MILLA       | DURHAM PANKY                |
| MILLA       | FLASH WARS                  |
| MILLA       | HIGH ENCINO                 |
| MILLA       | JERK PAYCHECK               |
| MILLA       | KRAMER CHOCOLATE            |
| MILLA       | LOVER TRUMAN                |
| MILLA       | MADIGAN DORADO              |
| MILLA       | NATURAL STOCK               |
| MILLA       | NOON PAPI                   |
| MILLA       | OPEN AFRICAN                |
| MILLA       | PATIENT SISTER              |
| MILLA       | PURE RUNNER                 |
| MILLA       | REDEMPTION COMFORTS         |
| MILLA       | ROXANNE REBEL               |
| MILLA       | SENSIBILITY REAR            |
| MILLA       | SLEEPING SUSPECTS           |
| MILLA       | SPOILERS HELLFIGHTERS       |
| MILLA       | SQUAD FISH                  |
| MILLA       | STONE FIRE                  |
| MILLA       | SWEET BROTHERHOOD           |
| MILLA       | TRADING PINOCCHIO           |
| MILLA       | WANDA CHAMBER               |
| BURT        | ALASKA PHANTOM              |
| BURT        | ARABIA DOGMA                |
| BURT        | CHILL LUCK                  |
| BURT        | COMMAND DARLING             |
| BURT        | DESERT POSEIDON             |
| BURT        | FAMILY SWEET                |
| BURT        | GAMES BOWFINGER             |
| BURT        | GRACELAND DYNAMITE          |
| BURT        | HOURS RAGE                  |
| BURT        | HYDE DOCTOR                 |
| BURT        | HYSTERICAL GRAIL            |
| BURT        | JUNGLE CLOSER               |
| BURT        | KILLER INNOCENT             |
| BURT        | LAMBS CINCINATTI            |
| BURT        | LUKE MUMMY                  |
| BURT        | MAGIC MALLRATS              |
| BURT        | MINDS TRUMAN                |
| BURT        | OTHERS SOUP                 |
| BURT        | PEACH INNOCENT              |
| BURT        | ROOTS REMEMBER              |
| BURT        | SATURDAY LAMBS              |
| BURT        | SENSIBILITY REAR            |
| BURT        | SWARM GOLD                  |
| BURT        | UNBREAKABLE KARATE          |
| ANGELINA    | BEAST HUNCHBACK             |
| ANGELINA    | BENEATH RUSH                |
| ANGELINA    | BETRAYED REAR               |
| ANGELINA    | BREAKFAST GOLDFINGER        |
| ANGELINA    | CARRIE BUNCH                |
| ANGELINA    | CRANES RESERVOIR            |
| ANGELINA    | DESIRE ALIEN                |
| ANGELINA    | DISTURBING SCARFACE         |
| ANGELINA    | DRAGONFLY STRANGERS         |
| ANGELINA    | GANDHI KWAI                 |
| ANGELINA    | HUSTLER PARTY               |
| ANGELINA    | INTENTIONS EMPIRE           |
| ANGELINA    | JADE BUNCH                  |
| ANGELINA    | KILLER INNOCENT             |
| ANGELINA    | MEMENTO ZOOLANDER           |
| ANGELINA    | MULAN MOON                  |
| ANGELINA    | MUMMY CREATURES             |
| ANGELINA    | ORDER BETRAYED              |
| ANGELINA    | OUTLAW HANKY                |
| ANGELINA    | PACIFIC AMISTAD             |
| ANGELINA    | RACER EGG                   |
| ANGELINA    | SAMURAI LION                |
| ANGELINA    | SATURN NAME                 |
| ANGELINA    | SEVEN SWARM                 |
| ANGELINA    | STORY SIDE                  |
| ANGELINA    | SUMMER SCARFACE             |
| ANGELINA    | SUNSET RACER                |
| ANGELINA    | SWARM GOLD                  |
| ANGELINA    | TROJAN TOMORROW             |
| ANGELINA    | VANISHED GARDEN             |
| ANGELINA    | WARDROBE PHANTOM            |
| CARY        | ALI FOREVER                 |
| CARY        | AMISTAD MIDSUMMER           |
| CARY        | ARMY FLINTSTONES            |
| CARY        | BINGO TALENTED              |
| CARY        | BLACKOUT PRIVATE            |
| CARY        | CITIZEN SHREK               |
| CARY        | DESPERATE TRAINSPOTTING     |
| CARY        | DOLLS RAGE                  |
| CARY        | DOUBLE WRATH                |
| CARY        | DUFFEL APOCALYPSE           |
| CARY        | FULL FLATLINERS             |
| CARY        | HUNTING MUSKETEERS          |
| CARY        | INDIAN LOVE                 |
| CARY        | LOVERBOY ATTACKS            |
| CARY        | MAUDE MOD                   |
| CARY        | MUSSOLINI SPOILERS          |
| CARY        | OKLAHOMA JUMANJI            |
| CARY        | PREJUDICE OLEANDER          |
| CARY        | RULES HUMAN                 |
| CARY        | VELVET TERMINATOR           |
| CARY        | VILLAIN DESPERATE           |
| CARY        | WATCH TRACY                 |
| CARY        | WEST LION                   |
| CARY        | WRONG BEHAVIOR              |
| GROUCHO     | BOOGIE AMELIE               |
| GROUCHO     | DOGMA FAMILY                |
| GROUCHO     | DUDE BLINDNESS              |
| GROUCHO     | DUFFEL APOCALYPSE           |
| GROUCHO     | DYING MAKER                 |
| GROUCHO     | FAMILY SWEET                |
| GROUCHO     | GUN BONNIE                  |
| GROUCHO     | HALLOWEEN NUTS              |
| GROUCHO     | HOMICIDE PEACH              |
| GROUCHO     | INDEPENDENCE HOTEL          |
| GROUCHO     | LABYRINTH LEAGUE            |
| GROUCHO     | LICENSE WEEKEND             |
| GROUCHO     | LORD ARIZONA                |
| GROUCHO     | MAGNOLIA FORRESTER          |
| GROUCHO     | MAJESTIC FLOATS             |
| GROUCHO     | MOTHER OLEANDER             |
| GROUCHO     | PELICAN COMFORTS            |
| GROUCHO     | PET HAUNTING                |
| GROUCHO     | POLLOCK DELIVERANCE         |
| GROUCHO     | SASSY PACKER                |
| GROUCHO     | SCALAWAG DUCK               |
| GROUCHO     | SMILE EARRING               |
| GROUCHO     | STRANGELOVE DESIRE          |
| GROUCHO     | TELEMARK HEARTBREAKERS      |
| GROUCHO     | WATCH TRACY                 |
| GROUCHO     | WEREWOLF LOLA               |
| MAE         | APOCALYPSE FLAMINGOS        |
| MAE         | APOLLO TEEN                 |
| MAE         | ARMY FLINTSTONES            |
| MAE         | CHICAGO NORTH               |
| MAE         | DANCES NONE                 |
| MAE         | DIARY PANIC                 |
| MAE         | DOOM DANCING                |
| MAE         | DUMBO LUST                  |
| MAE         | EAGLES PANKY                |
| MAE         | EARRING INSTINCT            |
| MAE         | FACTORY DRAGON              |
| MAE         | GOLDMINE TYCOON             |
| MAE         | HOMICIDE PEACH              |
| MAE         | HOOK CHARIOTS               |
| MAE         | JACKET FRISCO               |
| MAE         | MUPPET MILE                 |
| MAE         | NORTHWEST POLISH            |
| MAE         | ODDS BOOGIE                 |
| MAE         | OUTBREAK DIVINE             |
| MAE         | RESURRECTION SILVERADO      |
| MAE         | RUN PACIFIC                 |
| MAE         | RUSH GOODFELLAS             |
| MAE         | SCHOOL JACKET               |
| MAE         | SECRET GROUNDHOG            |
| MAE         | SHIP WONDERLAND             |
| MAE         | STAMPEDE DISTURBING         |
| MAE         | STRANGER STRANGERS          |
| MAE         | TURN STAR                   |
| RALPH       | BEVERLY OUTLAW              |
| RALPH       | CANYON STOCK                |
| RALPH       | CASPER DRAGONFLY            |
| RALPH       | CONFUSED CANDLES            |
| RALPH       | DANGEROUS UPTOWN            |
| RALPH       | DARN FORRESTER              |
| RALPH       | DUDE BLINDNESS              |
| RALPH       | DUMBO LUST                  |
| RALPH       | EMPIRE MALKOVICH            |
| RALPH       | FROST HEAD                  |
| RALPH       | FUGITIVE MAGUIRE            |
| RALPH       | FULL FLATLINERS             |
| RALPH       | GLORY TRACY                 |
| RALPH       | HOURS RAGE                  |
| RALPH       | JAPANESE RUN                |
| RALPH       | MAKER GABLES                |
| RALPH       | NEIGHBORS CHARADE           |
| RALPH       | NEWSIES STORY               |
| RALPH       | PINOCCHIO SIMON             |
| RALPH       | POCUS PULP                  |
| RALPH       | POLISH BROOKLYN             |
| RALPH       | RACER EGG                   |
| RALPH       | SHIP WONDERLAND             |
| RALPH       | SLEUTH ORIENT               |
| RALPH       | SUBMARINE BED               |
| RALPH       | THIN SAGEBRUSH              |
| RALPH       | VIDEOTAPE ARSENIC           |
| RALPH       | WITCHES PANIC               |
| SCARLETT    | AFFAIR PREJUDICE            |
| SCARLETT    | ALAMO VIDEOTAPE             |
| SCARLETT    | BEAR GRACELAND              |
| SCARLETT    | BORROWERS BEDAZZLED         |
| SCARLETT    | CONNECTION MICROCOSMOS      |
| SCARLETT    | CRAFT OUTFIELD              |
| SCARLETT    | CROW GREASE                 |
| SCARLETT    | DAWN POND                   |
| SCARLETT    | DEEP CRUSADE                |
| SCARLETT    | DIRTY ACE                   |
| SCARLETT    | DUDE BLINDNESS              |
| SCARLETT    | EAGLES PANKY                |
| SCARLETT    | EARLY HOME                  |
| SCARLETT    | FARGO GANDHI                |
| SCARLETT    | FRANKENSTEIN STRANGER       |
| SCARLETT    | GUNFIGHTER MUSSOLINI        |
| SCARLETT    | HANOVER GALAXY              |
| SCARLETT    | IMAGE PRINCESS              |
| SCARLETT    | INDIAN LOVE                 |
| SCARLETT    | INTERVIEW LIAISONS          |
| SCARLETT    | LABYRINTH LEAGUE            |
| SCARLETT    | LAMBS CINCINATTI            |
| SCARLETT    | LOLA AGENT                  |
| SCARLETT    | MADNESS ATTACKS             |
| SCARLETT    | MASSAGE IMAGE               |
| SCARLETT    | MILLION ACE                 |
| SCARLETT    | MINDS TRUMAN                |
| SCARLETT    | MYSTIC TRUMAN               |
| SCARLETT    | NEIGHBORS CHARADE           |
| SCARLETT    | ORIENT CLOSER               |
| SCARLETT    | POTLUCK MIXED               |
| SCARLETT    | RAGE GAMES                  |
| SCARLETT    | RIDER CADDYSHACK            |
| SCARLETT    | SANTA PARIS                 |
| SCARLETT    | SPICE SORORITY              |
| SCARLETT    | TREATMENT JEKYLL            |
| WOODY       | ALONE TRIP                  |
| WOODY       | APOLLO TEEN                 |
| WOODY       | BUGSY SONG                  |
| WOODY       | CHILL LUCK                  |
| WOODY       | CRAZY HOME                  |
| WOODY       | DOOM DANCING                |
| WOODY       | DOWNHILL ENOUGH             |
| WOODY       | EVERYONE CRAFT              |
| WOODY       | FEATHERS METAL              |
| WOODY       | FIRE WOLVES                 |
| WOODY       | FURY MURDER                 |
| WOODY       | IMAGE PRINCESS              |
| WOODY       | INVASION CYCLONE            |
| WOODY       | JEEPERS WEDDING             |
| WOODY       | KILL BROTHERHOOD            |
| WOODY       | KRAMER CHOCOLATE            |
| WOODY       | LOLA AGENT                  |
| WOODY       | MAIDEN HOME                 |
| WOODY       | MASK PEACH                  |
| WOODY       | RUN PACIFIC                 |
| WOODY       | SHINING ROSES               |
| WOODY       | SKY MIRACLE                 |
| WOODY       | STAGECOACH ARMAGEDDON       |
| WOODY       | STALLION SUNDANCE           |
| WOODY       | SWARM GOLD                  |
| WOODY       | TAXI KICK                   |
| WOODY       | TITANS JERK                 |
| WOODY       | TRIP NEWTON                 |
| WOODY       | WAKE JAWS                   |
| WOODY       | WISDOM WORKER               |
| WOODY       | WONDERLAND CHRISTMAS        |
| BEN         | BADMAN DAWN                 |
| BEN         | BALLROOM MOCKINGBIRD        |
| BEN         | BEACH HEARTBREAKERS         |
| BEN         | CABIN FLASH                 |
| BEN         | CARIBBEAN LIBERTY           |
| BEN         | CAROL TEXAS                 |
| BEN         | CHANCE RESURRECTION         |
| BEN         | COLDBLOODED DARLING         |
| BEN         | DAZED PUNK                  |
| BEN         | DOWNHILL ENOUGH             |
| BEN         | DRACULA CRYSTAL             |
| BEN         | DURHAM PANKY                |
| BEN         | EARLY HOME                  |
| BEN         | ELIZABETH SHANE             |
| BEN         | ENCINO ELF                  |
| BEN         | FROGMEN BREAKING            |
| BEN         | FRONTIER CABIN              |
| BEN         | GOODFELLAS SALUTE           |
| BEN         | HEAVYWEIGHTS BEAST          |
| BEN         | LIBERTY MAGNIFICENT         |
| BEN         | LONELY ELEPHANT             |
| BEN         | NASH CHOCOLAT               |
| BEN         | NOVOCAINE FLIGHT            |
| BEN         | PANTHER REDS                |
| BEN         | PERFECT GROOVE              |
| BEN         | PLUTO OLEANDER              |
| BEN         | RECORDS ZORRO               |
| BEN         | SATURDAY LAMBS              |
| BEN         | SECRETARY ROUGE             |
| BEN         | SHANGHAI TYCOON             |
| BEN         | SPLENDOR PATTON             |
| BEN         | SWEETHEARTS SUSPECTS        |
| BEN         | VALLEY PACKER               |
| JAMES       | AMADEUS HOLY                |
| JAMES       | ARMAGEDDON LOST             |
| JAMES       | AUTUMN CROW                 |
| JAMES       | CONFUSED CANDLES            |
| JAMES       | DOCTOR GRAIL                |
| JAMES       | ENCINO ELF                  |
| JAMES       | EVERYONE CRAFT              |
| JAMES       | FIDDLER LOST                |
| JAMES       | FIREBALL PHILADELPHIA       |
| JAMES       | HEDWIG ALTER                |
| JAMES       | HELLFIGHTERS SIERRA         |
| JAMES       | INNOCENT USUAL              |
| JAMES       | JEDI BENEATH                |
| JAMES       | JUMPING WRATH               |
| JAMES       | LONELY ELEPHANT             |
| JAMES       | LUCKY FLYING                |
| JAMES       | MAUDE MOD                   |
| JAMES       | MIDNIGHT WESTWARD           |
| JAMES       | MODERN DORADO               |
| JAMES       | NATIONAL STORY              |
| JAMES       | OUTBREAK DIVINE             |
| JAMES       | PUNK DIVORCE                |
| JAMES       | RIDER CADDYSHACK            |
| JAMES       | SATURDAY LAMBS              |
| JAMES       | SHAKESPEARE SADDLE          |
| JAMES       | SLIPPER FIDELITY            |
| JAMES       | SPIRIT FLINTSTONES          |
| JAMES       | STEEL SANTA                 |
| JAMES       | THIEF PELICAN               |
| JAMES       | WILLOW TRACY                |
| JAMES       | YOUNG LANGUAGE              |
| MINNIE      | ACE GOLDFINGER              |
| MINNIE      | ALICE FANTASIA              |
| MINNIE      | BILL OTHERS                 |
| MINNIE      | BONNIE HOLOCAUST            |
| MINNIE      | BOWFINGER GABLES            |
| MINNIE      | CHOCOLATE DUCK              |
| MINNIE      | DAY UNFAITHFUL              |
| MINNIE      | EVERYONE CRAFT              |
| MINNIE      | EXPRESS LONELY              |
| MINNIE      | EXTRAORDINARY CONQUERER     |
| MINNIE      | FRIDA SLIPPER               |
| MINNIE      | GROOVE FICTION              |
| MINNIE      | HOLIDAY GAMES               |
| MINNIE      | HYSTERICAL GRAIL            |
| MINNIE      | INSECTS STONE               |
| MINNIE      | JAPANESE RUN                |
| MINNIE      | JAWS HARRY                  |
| MINNIE      | LIFE TWISTED                |
| MINNIE      | MADIGAN DORADO              |
| MINNIE      | MANNEQUIN WORST             |
| MINNIE      | MONSOON CAUSE               |
| MINNIE      | NOTTING SPEAKEASY           |
| MINNIE      | PICKUP DRIVING              |
| MINNIE      | RAGING AIRPLANE             |
| MINNIE      | SANTA PARIS                 |
| MINNIE      | SMOKING BARBARELLA          |
| MINNIE      | SUSPECTS QUILLS             |
| MINNIE      | TALENTED HOMICIDE           |
| MINNIE      | TOMORROW HUSTLER            |
| MINNIE      | WAR NOTTING                 |
| MINNIE      | WARS PLUTO                  |
| GREG        | CHARADE DUFFEL              |
| GREG        | CLYDE THEORY                |
| GREG        | CRUELTY UNFORGIVEN          |
| GREG        | DAY UNFAITHFUL              |
| GREG        | DRACULA CRYSTAL             |
| GREG        | FANTASY TROOPERS            |
| GREG        | FORWARD TEMPLE              |
| GREG        | GODFATHER DIARY             |
| GREG        | HALF OUTFIELD               |
| GREG        | HOPE TOOTSIE                |
| GREG        | JEOPARDY ENCINO             |
| GREG        | JET NEIGHBORS               |
| GREG        | LIBERTY MAGNIFICENT         |
| GREG        | LICENSE WEEKEND             |
| GREG        | MAGNIFICENT CHITTY          |
| GREG        | NEWTON LABYRINTH            |
| GREG        | NOVOCAINE FLIGHT            |
| GREG        | OLEANDER CLUE               |
| GREG        | RUNNER MADIGAN              |
| GREG        | SAMURAI LION                |
| GREG        | SLING LUKE                  |
| GREG        | STRICTLY SCARFACE           |
| GREG        | TEEN APOLLO                 |
| GREG        | TITANS JERK                 |
| GREG        | TRAINSPOTTING STRANGERS     |
| GREG        | UNFAITHFUL KILL             |
| GREG        | USUAL UNTOUCHABLES          |
| SPENCER     | BACKLASH UNDEFEATED         |
| SPENCER     | CLOCKWORK PARADISE          |
| SPENCER     | CLUE GRAIL                  |
| SPENCER     | CUPBOARD SINNERS            |
| SPENCER     | DANGEROUS UPTOWN            |
| SPENCER     | DRAGON SQUAD                |
| SPENCER     | DRIFTER COMMANDMENTS        |
| SPENCER     | FIDDLER LOST                |
| SPENCER     | HOLIDAY GAMES               |
| SPENCER     | MERMAID INSECTS             |
| SPENCER     | MOTHER OLEANDER             |
| SPENCER     | MUMMY CREATURES             |
| SPENCER     | PANKY SUBMARINE             |
| SPENCER     | PILOT HOOSIERS              |
| SPENCER     | QUEEN LUKE                  |
| SPENCER     | REBEL AIRPORT               |
| SPENCER     | REDS POCUS                  |
| SPENCER     | SPIRIT FLINTSTONES          |
| SPENCER     | SWARM GOLD                  |
| SPENCER     | WAGON JAWS                  |
| SPENCER     | WASH HEAVENLY               |
| KENNETH     | AFFAIR PREJUDICE            |
| KENNETH     | BIRDCAGE CASPER             |
| KENNETH     | BOONDOCK BALLROOM           |
| KENNETH     | CATCH AMISTAD               |
| KENNETH     | COMMAND DARLING             |
| KENNETH     | CROSSROADS CASUALTIES       |
| KENNETH     | DISTURBING SCARFACE         |
| KENNETH     | FARGO GANDHI                |
| KENNETH     | MOURNING PURPLE             |
| KENNETH     | NEMO CAMPUS                 |
| KENNETH     | PEAK FOREVER                |
| KENNETH     | REAR TRADING                |
| KENNETH     | SHAWSHANK BUBBLE            |
| KENNETH     | SONG HEDWIG                 |
| KENNETH     | STALLION SUNDANCE           |
| KENNETH     | TEMPLE ATTRACTION           |
| KENNETH     | TRAP GUYS                   |
| KENNETH     | USUAL UNTOUCHABLES          |
| KENNETH     | VICTORY ACADEMY             |
| KENNETH     | WEREWOLF LOLA               |
| CHARLIZE    | BABY HALL                   |
| CHARLIZE    | BUCKET BROTHERHOOD          |
| CHARLIZE    | CANDLES GRAPES              |
| CHARLIZE    | CLUELESS BUCKET             |
| CHARLIZE    | CONTROL ANTHEM              |
| CHARLIZE    | CRANES RESERVOIR            |
| CHARLIZE    | DARN FORRESTER              |
| CHARLIZE    | DRIVER ANNIE                |
| CHARLIZE    | DYNAMITE TARZAN             |
| CHARLIZE    | FEATHERS METAL              |
| CHARLIZE    | FUGITIVE MAGUIRE            |
| CHARLIZE    | HAUNTING PIANIST            |
| CHARLIZE    | HEAVEN FREEDOM              |
| CHARLIZE    | HYSTERICAL GRAIL            |
| CHARLIZE    | JACKET FRISCO               |
| CHARLIZE    | JOON NORTHWEST              |
| CHARLIZE    | LONELY ELEPHANT             |
| CHARLIZE    | LUST LOCK                   |
| CHARLIZE    | MASSAGE IMAGE               |
| CHARLIZE    | PRIMARY GLASS               |
| CHARLIZE    | SPLENDOR PATTON             |
| CHARLIZE    | SUNDANCE INVASION           |
| CHARLIZE    | WESTWARD SEABISCUIT         |
| CHARLIZE    | WIND PHANTOM                |
| SEAN        | ACE GOLDFINGER              |
| SEAN        | ALAMO VIDEOTAPE             |
| SEAN        | BROOKLYN DESERT             |
| SEAN        | CRUSADE HONEY               |
| SEAN        | DARN FORRESTER              |
| SEAN        | DUMBO LUST                  |
| SEAN        | FANTASY TROOPERS            |
| SEAN        | FORRESTER COMANCHEROS       |
| SEAN        | GO PURPLE                   |
| SEAN        | GRAFFITI LOVE               |
| SEAN        | GROSSE WONDERFUL            |
| SEAN        | GROUNDHOG UNCUT             |
| SEAN        | HALF OUTFIELD               |
| SEAN        | HAUNTING PIANIST            |
| SEAN        | HORN WORKING                |
| SEAN        | HUNTING MUSKETEERS          |
| SEAN        | IGBY MAKER                  |
| SEAN        | LICENSE WEEKEND             |
| SEAN        | LONELY ELEPHANT             |
| SEAN        | LUST LOCK                   |
| SEAN        | MOCKINGBIRD HOLLYWOOD       |
| SEAN        | OCTOBER SUBMARINE           |
| SEAN        | PATIENT SISTER              |
| SEAN        | PHILADELPHIA WIFE           |
| SEAN        | SCORPION APOLLO             |
| SEAN        | SOLDIERS EVOLUTION          |
| SEAN        | STAGECOACH ARMAGEDDON       |
| SEAN        | STREAK RIDGEMONT            |
| SEAN        | SUBMARINE BED               |
| SEAN        | SUPERFLY TRIP               |
| SEAN        | TELEMARK HEARTBREAKERS      |
| SEAN        | TRACY CIDER                 |
| SEAN        | UNITED PILOT                |
| CHRISTOPHER | ALI FOREVER                 |
| CHRISTOPHER | ANGELS LIFE                 |
| CHRISTOPHER | BACKLASH UNDEFEATED         |
| CHRISTOPHER | CONGENIALITY QUEST          |
| CHRISTOPHER | CONTACT ANONYMOUS           |
| CHRISTOPHER | CREEPERS KANE               |
| CHRISTOPHER | FREEDOM CLEOPATRA           |
| CHRISTOPHER | HIGHBALL POTTER             |
| CHRISTOPHER | ICE CROSSING                |
| CHRISTOPHER | JEEPERS WEDDING             |
| CHRISTOPHER | KANE EXORCIST               |
| CHRISTOPHER | LANGUAGE COWBOY             |
| CHRISTOPHER | LAWRENCE LOVE               |
| CHRISTOPHER | MURDER ANTITRUST            |
| CHRISTOPHER | SLEUTH ORIENT               |
| CHRISTOPHER | SPINAL ROCKY                |
| CHRISTOPHER | STORM HAPPINESS             |
| CHRISTOPHER | SUGAR WONKA                 |
| CHRISTOPHER | VIDEOTAPE ARSENIC           |
| CHRISTOPHER | WOMEN DORADO                |
| KIRSTEN     | BOULEVARD MOB               |
| KIRSTEN     | BRAVEHEART HUMAN            |
| KIRSTEN     | BUCKET BROTHERHOOD          |
| KIRSTEN     | BUGSY SONG                  |
| KIRSTEN     | CASABLANCA SUPER            |
| KIRSTEN     | CHARADE DUFFEL              |
| KIRSTEN     | DANGEROUS UPTOWN            |
| KIRSTEN     | DEVIL DESIRE                |
| KIRSTEN     | FRISCO FORREST              |
| KIRSTEN     | GRINCH MASSAGE              |
| KIRSTEN     | HOURS RAGE                  |
| KIRSTEN     | HURRICANE AFFAIR            |
| KIRSTEN     | IMAGE PRINCESS              |
| KIRSTEN     | ISHTAR ROCKETEER            |
| KIRSTEN     | LABYRINTH LEAGUE            |
| KIRSTEN     | LEAGUE HELLFIGHTERS         |
| KIRSTEN     | MADIGAN DORADO              |
| KIRSTEN     | MADNESS ATTACKS             |
| KIRSTEN     | MAGIC MALLRATS              |
| KIRSTEN     | MAKER GABLES                |
| KIRSTEN     | MASSAGE IMAGE               |
| KIRSTEN     | MEMENTO ZOOLANDER           |
| KIRSTEN     | NECKLACE OUTBREAK           |
| KIRSTEN     | PATHS CONTROL               |
| KIRSTEN     | PLUTO OLEANDER              |
| KIRSTEN     | PRIVATE DROP                |
| KIRSTEN     | RAIDERS ANTITRUST           |
| KIRSTEN     | REUNION WITCHES             |
| KIRSTEN     | SKY MIRACLE                 |
| KIRSTEN     | SPEAKEASY DATE              |
| KIRSTEN     | STAGECOACH ARMAGEDDON       |
| KIRSTEN     | TIES HUNGER                 |
| KIRSTEN     | USUAL UNTOUCHABLES          |
| KIRSTEN     | WORST BANGER                |
| ELLEN       | BILKO ANONYMOUS             |
| ELLEN       | CARIBBEAN LIBERTY           |
| ELLEN       | CASPER DRAGONFLY            |
| ELLEN       | EMPIRE MALKOVICH            |
| ELLEN       | FLOATS GARDEN               |
| ELLEN       | FROGMEN BREAKING            |
| ELLEN       | HOMEWARD CIDER              |
| ELLEN       | HYDE DOCTOR                 |
| ELLEN       | IMAGE PRINCESS              |
| ELLEN       | JACKET FRISCO               |
| ELLEN       | MICROCOSMOS PARADISE        |
| ELLEN       | NETWORK PEAK                |
| ELLEN       | OSCAR GOLD                  |
| ELLEN       | PICKUP DRIVING              |
| ELLEN       | PINOCCHIO SIMON             |
| ELLEN       | PRIVATE DROP                |
| ELLEN       | ROOTS REMEMBER              |
| ELLEN       | SCARFACE BANG               |
| ELLEN       | SECRETARY ROUGE             |
| ELLEN       | SPY MILE                    |
| ELLEN       | STREETCAR INTENTIONS        |
| ELLEN       | TADPOLE PARK                |
| ELLEN       | TREASURE COMMAND            |
| ELLEN       | TURN STAR                   |
| ELLEN       | WOMEN DORADO                |
| KENNETH     | ALI FOREVER                 |
| KENNETH     | BEAST HUNCHBACK             |
| KENNETH     | BIRDCAGE CASPER             |
| KENNETH     | CARRIE BUNCH                |
| KENNETH     | CITIZEN SHREK               |
| KENNETH     | CROSSROADS CASUALTIES       |
| KENNETH     | DANCING FEVER               |
| KENNETH     | DETECTIVE VISION            |
| KENNETH     | EARTH VISION                |
| KENNETH     | EGYPT TENENBAUMS            |
| KENNETH     | FLAMINGOS CONNECTICUT       |
| KENNETH     | FLATLINERS KILLER           |
| KENNETH     | FRIDA SLIPPER               |
| KENNETH     | GHOST GROUNDHOG             |
| KENNETH     | HARPER DYING                |
| KENNETH     | HOMICIDE PEACH              |
| KENNETH     | INDEPENDENCE HOTEL          |
| KENNETH     | JACKET FRISCO               |
| KENNETH     | JAPANESE RUN                |
| KENNETH     | LEAGUE HELLFIGHTERS         |
| KENNETH     | LESSON CLEOPATRA            |
| KENNETH     | LIES TREATMENT              |
| KENNETH     | LOST BIRD                   |
| KENNETH     | LUCKY FLYING                |
| KENNETH     | MAGNIFICENT CHITTY          |
| KENNETH     | MAIDEN HOME                 |
| KENNETH     | RAIDERS ANTITRUST           |
| KENNETH     | RAINBOW SHOCK               |
| KENNETH     | REMEMBER DIARY              |
| KENNETH     | SEATTLE EXPECATIONS         |
| KENNETH     | SHIP WONDERLAND             |
| KENNETH     | VOLUME HOUSE                |
| KENNETH     | WORKING MICROCOSMOS         |
| DARYL       | AMISTAD MIDSUMMER           |
| DARYL       | ARACHNOPHOBIA ROLLERCOASTER |
| DARYL       | BABY HALL                   |
| DARYL       | BALLROOM MOCKINGBIRD        |
| DARYL       | BEHAVIOR RUNAWAY            |
| DARYL       | BIRCH ANTITRUST             |
| DARYL       | CASUALTIES ENCINO           |
| DARYL       | DANGEROUS UPTOWN            |
| DARYL       | DOUBLE WRATH                |
| DARYL       | EXPECATIONS NATURAL         |
| DARYL       | FAMILY SWEET                |
| DARYL       | FIDDLER LOST                |
| DARYL       | FORREST SONS                |
| DARYL       | GENTLEMEN STAGE             |
| DARYL       | GRAIL FRANKENSTEIN          |
| DARYL       | HOLES BRANNIGAN             |
| DARYL       | HOLOCAUST HIGHBALL          |
| DARYL       | HOOSIERS BIRDCAGE           |
| DARYL       | KILLER INNOCENT             |
| DARYL       | LIFE TWISTED                |
| DARYL       | MADRE GABLES                |
| DARYL       | MAIDEN HOME                 |
| DARYL       | NEIGHBORS CHARADE           |
| DARYL       | NORTH TEQUILA               |
| DARYL       | POND SEATTLE                |
| DARYL       | RUGRATS SHAKESPEARE         |
| DARYL       | SMOOCHY CONTROL             |
| DARYL       | SPIKING ELEMENT             |
| DARYL       | STREAK RIDGEMONT            |
| DARYL       | TRAFFIC HOBBIT              |
| DARYL       | UNFAITHFUL KILL             |
| GENE        | AIRPORT POLLOCK             |
| GENE        | ARGONAUTS TOWN              |
| GENE        | ARMY FLINTSTONES            |
| GENE        | BANGER PINOCCHIO            |
| GENE        | BEACH HEARTBREAKERS         |
| GENE        | BENEATH RUSH                |
| GENE        | CHAMPION FLATLINERS         |
| GENE        | DARKNESS WAR                |
| GENE        | DORADO NOTTING              |
| GENE        | FLAMINGOS CONNECTICUT       |
| GENE        | HOOK CHARIOTS               |
| GENE        | ILLUSION AMELIE             |
| GENE        | JET NEIGHBORS               |
| GENE        | METROPOLIS COMA             |
| GENE        | MONEY HAROLD                |
| GENE        | PAST SUICIDES               |
| GENE        | SECRETS PARADISE            |
| GENE        | SPLASH GUMP                 |
| GENE        | STING PERSONAL              |
| GENE        | TADPOLE PARK                |
| GENE        | VIRGINIAN PLUTO             |
| GENE        | WEREWOLF LOLA               |
| GENE        | WORDS HUNTER                |
| MEG         | CHILL LUCK                  |
| MEG         | CONNECTICUT TRAMP           |
| MEG         | CRAZY HOME                  |
| MEG         | CRUSADE HONEY               |
| MEG         | DROP WATERFRONT             |
| MEG         | FIDDLER LOST                |
| MEG         | FUGITIVE MAGUIRE            |
| MEG         | GANDHI KWAI                 |
| MEG         | GILMORE BOILED              |
| MEG         | GORGEOUS BINGO              |
| MEG         | HOUSE DYNAMITE              |
| MEG         | HYSTERICAL GRAIL            |
| MEG         | INTOLERABLE INTENTIONS      |
| MEG         | LIAISONS SWEET              |
| MEG         | MAKER GABLES                |
| MEG         | MASK PEACH                  |
| MEG         | ORANGE GRAPES               |
| MEG         | PAPI NECKLACE               |
| MEG         | REUNION WITCHES             |
| MEG         | SABRINA MIDNIGHT            |
| MEG         | SAGEBRUSH CLUELESS          |
| MEG         | SPEED SUIT                  |
| MEG         | SUMMER SCARFACE             |
| MEG         | VACATION BOONDOCK           |
| MEG         | VAMPIRE WHALE               |
| MEG         | VISION TORQUE               |
| MEG         | VOYAGE LEGALLY              |
| CHRIS       | BENEATH RUSH                |
| CHRIS       | BILL OTHERS                 |
| CHRIS       | BLINDNESS GUN               |
| CHRIS       | BOONDOCK BALLROOM           |
| CHRIS       | BUNCH MINDS                 |
| CHRIS       | CARIBBEAN LIBERTY           |
| CHRIS       | CONVERSATION DOWNHILL       |
| CHRIS       | CROW GREASE                 |
| CHRIS       | DARN FORRESTER              |
| CHRIS       | EXTRAORDINARY CONQUERER     |
| CHRIS       | MUPPET MILE                 |
| CHRIS       | ODDS BOOGIE                 |
| CHRIS       | PLUTO OLEANDER              |
| CHRIS       | PURPLE MOVIE                |
| CHRIS       | RAGE GAMES                  |
| CHRIS       | REDS POCUS                  |
| CHRIS       | REQUIEM TYCOON              |
| CHRIS       | ROAD ROXANNE                |
| CHRIS       | ROCKETEER MOTHER            |
| CHRIS       | SATURN NAME                 |
| CHRIS       | SHAKESPEARE SADDLE          |
| CHRIS       | SPARTACUS CHEAPER           |
| CHRIS       | SPINAL ROCKY                |
| CHRIS       | TROJAN TOMORROW             |
| CHRIS       | WALLS ARTIST                |
| CHRIS       | WONDERLAND CHRISTMAS        |
| CHRIS       | WORLD LEATHERNECKS          |
| JIM         | AIRPLANE SIERRA             |
| JIM         | ANONYMOUS HUMAN             |
| JIM         | BOILED DARES                |
| JIM         | DRAGON SQUAD                |
| JIM         | FLATLINERS KILLER           |
| JIM         | FLOATS GARDEN               |
| JIM         | GRINCH MASSAGE              |
| JIM         | HELLFIGHTERS SIERRA         |
| JIM         | JAPANESE RUN                |
| JIM         | JUMANJI BLADE               |
| JIM         | LEAGUE HELLFIGHTERS         |
| JIM         | LUCKY FLYING                |
| JIM         | METROPOLIS COMA             |
| JIM         | MOTIONS DETAILS             |
| JIM         | NECKLACE OUTBREAK           |
| JIM         | NEMO CAMPUS                 |
| JIM         | NEWSIES STORY               |
| JIM         | OLEANDER CLUE               |
| JIM         | PERFECT GROOVE              |
| JIM         | RESERVOIR ADAPTATION        |
| JIM         | ROMAN PUNK                  |
| JIM         | SIERRA DIVIDE               |
| JIM         | SPY MILE                    |
| JIM         | WEEKEND PERSONAL            |
| JIM         | WISDOM WORKER               |
| JIM         | WOMEN DORADO                |
| SPENCER     | ALONE TRIP                  |
| SPENCER     | CANYON STOCK                |
| SPENCER     | DRAGON SQUAD                |
| SPENCER     | HEAVENLY GUN                |
| SPENCER     | HELLFIGHTERS SIERRA         |
| SPENCER     | LEATHERNECKS DWARFS         |
| SPENCER     | MASSACRE USUAL              |
| SPENCER     | ORDER BETRAYED              |
| SPENCER     | RANDOM GO                   |
| SPENCER     | REBEL AIRPORT               |
| SPENCER     | SALUTE APOLLO               |
| SPENCER     | SENSE GREEK                 |
| SPENCER     | SNATCHERS MONTEZUMA         |
| SPENCER     | STING PERSONAL              |
| SPENCER     | STORY SIDE                  |
| SPENCER     | SWEET BROTHERHOOD           |
| SPENCER     | TAXI KICK                   |
| SPENCER     | TREASURE COMMAND            |
| SPENCER     | TYCOON GATHERING            |
| SPENCER     | VIRGIN DAISY                |
| SPENCER     | WEEKEND PERSONAL            |
| SPENCER     | WITCHES PANIC               |
| SPENCER     | WORST BANGER                |
| SPENCER     | WRATH MILE                  |
| SUSAN       | BEAST HUNCHBACK             |
| SUSAN       | BENEATH RUSH                |
| SUSAN       | BONNIE HOLOCAUST            |
| SUSAN       | CHITTY LOCK                 |
| SUSAN       | CREATURES SHAKESPEARE       |
| SUSAN       | DRAGON SQUAD                |
| SUSAN       | DRIVING POLISH              |
| SUSAN       | DURHAM PANKY                |
| SUSAN       | EGYPT TENENBAUMS            |
| SUSAN       | EVE RESURRECTION            |
| SUSAN       | JUMPING WRATH               |
| SUSAN       | KARATE MOON                 |
| SUSAN       | LAWRENCE LOVE               |
| SUSAN       | MEMENTO ZOOLANDER           |
| SUSAN       | MURDER ANTITRUST            |
| SUSAN       | NATURAL STOCK               |
| SUSAN       | PANTHER REDS                |
| SUSAN       | PATHS CONTROL               |
| SUSAN       | PRIX UNDEFEATED             |
| SUSAN       | PULP BEVERLY                |
| SUSAN       | SAINTS BRIDE                |
| SUSAN       | SEARCHERS WAIT              |
| SUSAN       | SHINING ROSES               |
| SUSAN       | SPIKING ELEMENT             |
| SUSAN       | STAR OPERATION              |
| SUSAN       | UPTOWN YOUNG                |
| SUSAN       | VALLEY PACKER               |
| SUSAN       | VANISHING ROCKY             |
| SUSAN       | VIDEOTAPE ARSENIC           |
| SUSAN       | WISDOM WORKER               |
| SUSAN       | WIZARD COLDBLOODED          |
| SUSAN       | WONDERFUL DROP              |
| SUSAN       | WORKER TARZAN               |
| WALTER      | AMELIE HELLFIGHTERS         |
| WALTER      | ARABIA DOGMA                |
| WALTER      | BANG KWAI                   |
| WALTER      | CASABLANCA SUPER            |
| WALTER      | CASPER DRAGONFLY            |
| WALTER      | CROW GREASE                 |
| WALTER      | CURTAIN VIDEOTAPE           |
| WALTER      | DANCES NONE                 |
| WALTER      | EARLY HOME                  |
| WALTER      | FLYING HOOK                 |
| WALTER      | FORREST SONS                |
| WALTER      | FREDDY STORM                |
| WALTER      | GASLIGHT CRUSADE            |
| WALTER      | HOBBIT ALIEN                |
| WALTER      | HOOSIERS BIRDCAGE           |
| WALTER      | HYSTERICAL GRAIL            |
| WALTER      | JERSEY SASSY                |
| WALTER      | LAMBS CINCINATTI            |
| WALTER      | LESSON CLEOPATRA            |
| WALTER      | LIES TREATMENT              |
| WALTER      | LOCK REAR                   |
| WALTER      | LONELY ELEPHANT             |
| WALTER      | MADISON TRAP                |
| WALTER      | MOTIONS DETAILS             |
| WALTER      | MULHOLLAND BEAST            |
| WALTER      | MUMMY CREATURES             |
| WALTER      | NIGHTMARE CHILL             |
| WALTER      | NOVOCAINE FLIGHT            |
| WALTER      | RAIDERS ANTITRUST           |
| WALTER      | REUNION WITCHES             |
| WALTER      | ROOTS REMEMBER              |
| WALTER      | SIERRA DIVIDE               |
| WALTER      | SKY MIRACLE                 |
| WALTER      | SLUMS DUCK                  |
| WALTER      | SPIKING ELEMENT             |
| WALTER      | STAGE WORLD                 |
| WALTER      | STEPMOM DREAM               |
| WALTER      | STRANGELOVE DESIRE          |
| WALTER      | WARDROBE PHANTOM            |
| WALTER      | WITCHES PANIC               |
| WALTER      | WIZARD COLDBLOODED          |
| MATTHEW     | AFRICAN EGG                 |
| MATTHEW     | CANYON STOCK                |
| MATTHEW     | CELEBRITY HORN              |
| MATTHEW     | CRUSADE HONEY               |
| MATTHEW     | CUPBOARD SINNERS            |
| MATTHEW     | DANCING FEVER               |
| MATTHEW     | DAWN POND                   |
| MATTHEW     | DELIVERANCE MULHOLLAND      |
| MATTHEW     | EASY GLADIATOR              |
| MATTHEW     | ENGLISH BULWORTH            |
| MATTHEW     | FINDING ANACONDA            |
| MATTHEW     | FIREHOUSE VIETNAM           |
| MATTHEW     | FREAKY POCUS                |
| MATTHEW     | GAMES BOWFINGER             |
| MATTHEW     | GIANT TROOPERS              |
| MATTHEW     | GLASS DYING                 |
| MATTHEW     | GREATEST NORTH              |
| MATTHEW     | HOUSE DYNAMITE              |
| MATTHEW     | MOB DUFFEL                  |
| MATTHEW     | MUSCLE BRIGHT               |
| MATTHEW     | OPPOSITE NECKLACE           |
| MATTHEW     | ORIENT CLOSER               |
| MATTHEW     | POTLUCK MIXED               |
| MATTHEW     | ROBBERS JOON                |
| MATTHEW     | SOUP WISDOM                 |
| MATTHEW     | TOMORROW HUSTLER            |
| MATTHEW     | TRAFFIC HOBBIT              |
| MATTHEW     | TROJAN TOMORROW             |
| MATTHEW     | VIETNAM SMOOCHY             |
| MATTHEW     | WANDA CHAMBER               |
| PENELOPE    | AMADEUS HOLY                |
| PENELOPE    | ARMAGEDDON LOST             |
| PENELOPE    | ARMY FLINTSTONES            |
| PENELOPE    | BEAR GRACELAND              |
| PENELOPE    | BIKINI BORROWERS            |
| PENELOPE    | CHAPLIN LICENSE             |
| PENELOPE    | CLERKS ANGELS               |
| PENELOPE    | CORE SUIT                   |
| PENELOPE    | CRYSTAL BREAKING            |
| PENELOPE    | DISCIPLE MOTHER             |
| PENELOPE    | DUCK RACER                  |
| PENELOPE    | ENTRAPMENT SATISFACTION     |
| PENELOPE    | FEUD FROGMEN                |
| PENELOPE    | FIDELITY DEVIL              |
| PENELOPE    | HAMLET WISDOM               |
| PENELOPE    | HAROLD FRENCH               |
| PENELOPE    | INSTINCT AIRPORT            |
| PENELOPE    | LADY STAGE                  |
| PENELOPE    | LEGEND JEDI                 |
| PENELOPE    | MISSION ZOOLANDER           |
| PENELOPE    | MOTIONS DETAILS             |
| PENELOPE    | MUPPET MILE                 |
| PENELOPE    | PARADISE SABRINA            |
| PENELOPE    | PIANIST OUTFIELD            |
| PENELOPE    | ROCKY WAR                   |
| PENELOPE    | TITANIC BOONDOCK            |
| PENELOPE    | TRAIN BUNCH                 |
| PENELOPE    | UNTOUCHABLES SUNRISE        |
| PENELOPE    | VIRGINIAN PLUTO             |
| PENELOPE    | WONDERFUL DROP              |
| PENELOPE    | ZOOLANDER FICTION           |
| SIDNEY      | ALASKA PHANTOM              |
| SIDNEY      | ALIEN CENTER                |
| SIDNEY      | AMERICAN CIRCUS             |
| SIDNEY      | ANTITRUST TOMATOES          |
| SIDNEY      | ARTIST COLDBLOODED          |
| SIDNEY      | CANDIDATE PERDITION         |
| SIDNEY      | CLONES PINOCCHIO            |
| SIDNEY      | DOGMA FAMILY                |
| SIDNEY      | EMPIRE MALKOVICH            |
| SIDNEY      | ENDING CROWDS               |
| SIDNEY      | FINDING ANACONDA            |
| SIDNEY      | FREAKY POCUS                |
| SIDNEY      | GRACELAND DYNAMITE          |
| SIDNEY      | GREASE YOUTH                |
| SIDNEY      | LORD ARIZONA                |
| SIDNEY      | MANNEQUIN WORST             |
| SIDNEY      | MASK PEACH                  |
| SIDNEY      | MUMMY CREATURES             |
| SIDNEY      | OZ LIAISONS                 |
| SIDNEY      | PLUTO OLEANDER              |
| SIDNEY      | RUN PACIFIC                 |
| SIDNEY      | SIEGE MADRE                 |
| SIDNEY      | SPIRITED CASUALTIES         |
| SIDNEY      | SPY MILE                    |
| SIDNEY      | SUBMARINE BED               |
| SIDNEY      | SUNDANCE INVASION           |
| SIDNEY      | TITANS JERK                 |
| SIDNEY      | TRAMP OTHERS                |
| SIDNEY      | TREATMENT JEKYLL            |
| SIDNEY      | TRUMAN CRAZY                |
| SIDNEY      | WAKE JAWS                   |
| SIDNEY      | WORLD LEATHERNECKS          |
| SIDNEY      | WRONG BEHAVIOR              |
| SIDNEY      | WYOMING STORM               |
| GROUCHO     | ATTACKS HATE                |
| GROUCHO     | BLUES INSTINCT              |
| GROUCHO     | BUTCH PANTHER               |
| GROUCHO     | CASUALTIES ENCINO           |
| GROUCHO     | CHAPLIN LICENSE             |
| GROUCHO     | COLOR PHILADELPHIA          |
| GROUCHO     | CREATURES SHAKESPEARE       |
| GROUCHO     | CROW GREASE                 |
| GROUCHO     | DALMATIONS SWEDEN           |
| GROUCHO     | DEVIL DESIRE                |
| GROUCHO     | DONNIE ALLEY                |
| GROUCHO     | GABLES METROPOLIS           |
| GROUCHO     | GOLD RIVER                  |
| GROUCHO     | HAPPINESS UNITED            |
| GROUCHO     | HUNCHBACK IMPOSSIBLE        |
| GROUCHO     | INDEPENDENCE HOTEL          |
| GROUCHO     | IRON MOON                   |
| GROUCHO     | KISS GLORY                  |
| GROUCHO     | LABYRINTH LEAGUE            |
| GROUCHO     | MARRIED GO                  |
| GROUCHO     | MAUDE MOD                   |
| GROUCHO     | MOB DUFFEL                  |
| GROUCHO     | OPPOSITE NECKLACE           |
| GROUCHO     | PANKY SUBMARINE             |
| GROUCHO     | PARK CITIZEN                |
| GROUCHO     | PHANTOM GLORY               |
| GROUCHO     | POCUS PULP                  |
| GROUCHO     | RUNNER MADIGAN              |
| GROUCHO     | SATISFACTION CONFIDENTIAL   |
| GROUCHO     | SENSIBILITY REAR            |
| GROUCHO     | SUBMARINE BED               |
| GROUCHO     | SUNSET RACER                |
| GROUCHO     | TEMPLE ATTRACTION           |
| GROUCHO     | TOMATOES HELLFIGHTERS       |
| GROUCHO     | VANILLA DAY                 |
| GINA        | BED HIGHBALL                |
| GINA        | CALENDAR GUNFIGHT           |
| GINA        | CHAMBER ITALIAN             |
| GINA        | CHAPLIN LICENSE             |
| GINA        | CHARIOTS CONSPIRACY         |
| GINA        | CLUELESS BUCKET             |
| GINA        | COLDBLOODED DARLING         |
| GINA        | CONEHEADS SMOOCHY           |
| GINA        | DARKNESS WAR                |
| GINA        | DEER VIRGINIAN              |
| GINA        | DOGMA FAMILY                |
| GINA        | ELEPHANT TROJAN             |
| GINA        | EXCITEMENT EVE              |
| GINA        | FRISCO FORREST              |
| GINA        | GANDHI KWAI                 |
| GINA        | GOODFELLAS SALUTE           |
| GINA        | GUNFIGHT MOON               |
| GINA        | HALL CASSIDY                |
| GINA        | HEARTBREAKERS BRIGHT        |
| GINA        | HOOK CHARIOTS               |
| GINA        | HYDE DOCTOR                 |
| GINA        | IMPACT ALADDIN              |
| GINA        | INDIAN LOVE                 |
| GINA        | INTRIGUE WORST              |
| GINA        | LICENSE WEEKEND             |
| GINA        | LOUISIANA HARRY             |
| GINA        | MAGNIFICENT CHITTY          |
| GINA        | METAL ARMAGEDDON            |
| GINA        | MIDNIGHT WESTWARD           |
| GINA        | MOVIE SHAKESPEARE           |
| GINA        | MUMMY CREATURES             |
| GINA        | OPEN AFRICAN                |
| GINA        | SEARCHERS WAIT              |
| GINA        | SEVEN SWARM                 |
| GINA        | SIERRA DIVIDE               |
| GINA        | SPIRITED CASUALTIES         |
| GINA        | STORM HAPPINESS             |
| GINA        | SUGAR WONKA                 |
| GINA        | TELEGRAPH VOYAGE            |
| GINA        | TRAINSPOTTING STRANGERS     |
| GINA        | WIFE TURN                   |
| GINA        | WINDOW SIDE                 |
| WARREN      | ACADEMY DINOSAUR            |
| WARREN      | AGENT TRUMAN                |
| WARREN      | ALABAMA DEVIL               |
| WARREN      | CHARADE DUFFEL              |
| WARREN      | DARES PLUTO                 |
| WARREN      | DEEP CRUSADE                |
| WARREN      | DOOM DANCING                |
| WARREN      | ELF MURDER                  |
| WARREN      | FANTASIA PARK               |
| WARREN      | GARDEN ISLAND               |
| WARREN      | GREATEST NORTH              |
| WARREN      | GREEDY ROOTS                |
| WARREN      | KENTUCKIAN GIANT            |
| WARREN      | LADYBUGS ARMAGEDDON         |
| WARREN      | LESSON CLEOPATRA            |
| WARREN      | MASK PEACH                  |
| WARREN      | MEET CHOCOLATE              |
| WARREN      | OUTLAW HANKY                |
| WARREN      | PAJAMA JAWBREAKER           |
| WARREN      | PANTHER REDS                |
| WARREN      | PERSONAL LADYBUGS           |
| WARREN      | POTTER CONNECTICUT          |
| WARREN      | PRIDE ALAMO                 |
| WARREN      | PULP BEVERLY                |
| WARREN      | REDS POCUS                  |
| WARREN      | RIVER OUTLAW                |
| WARREN      | ROMAN PUNK                  |
| WARREN      | ROOTS REMEMBER              |
| WARREN      | THIEF PELICAN               |
| WARREN      | TITANIC BOONDOCK            |
| WARREN      | TOMATOES HELLFIGHTERS       |
| WARREN      | UNBREAKABLE KARATE          |
| WARREN      | WARDROBE PHANTOM            |
| WARREN      | WEDDING APOLLO              |
| SYLVESTER   | ALASKA PHANTOM              |
| SYLVESTER   | BACKLASH UNDEFEATED         |
| SYLVESTER   | BIRDS PERDITION             |
| SYLVESTER   | CLOCKWORK PARADISE          |
| SYLVESTER   | CONFIDENTIAL INTERVIEW      |
| SYLVESTER   | CREEPERS KANE               |
| SYLVESTER   | DOORS PRESIDENT             |
| SYLVESTER   | ENCINO ELF                  |
| SYLVESTER   | HALLOWEEN NUTS              |
| SYLVESTER   | INSTINCT AIRPORT            |
| SYLVESTER   | NEWSIES STORY               |
| SYLVESTER   | PARADISE SABRINA            |
| SYLVESTER   | PREJUDICE OLEANDER          |
| SYLVESTER   | PRIX UNDEFEATED             |
| SYLVESTER   | RINGS HEARTBREAKERS         |
| SYLVESTER   | RUSH GOODFELLAS             |
| SYLVESTER   | SHAWSHANK BUBBLE            |
| SYLVESTER   | SHEPHERD MIDSUMMER          |
| SYLVESTER   | SUN CONFESSIONS             |
| SYLVESTER   | TEXAS WATCH                 |
| SYLVESTER   | WALLS ARTIST                |
| SYLVESTER   | WEEKEND PERSONAL            |
| SUSAN       | AIRPORT POLLOCK             |
| SUSAN       | ANONYMOUS HUMAN             |
| SUSAN       | BED HIGHBALL                |
| SUSAN       | CARIBBEAN LIBERTY           |
| SUSAN       | CASUALTIES ENCINO           |
| SUSAN       | CLERKS ANGELS               |
| SUSAN       | EXCITEMENT EVE              |
| SUSAN       | FULL FLATLINERS             |
| SUSAN       | GLASS DYING                 |
| SUSAN       | GOODFELLAS SALUTE           |
| SUSAN       | HOTEL HAPPINESS             |
| SUSAN       | LEATHERNECKS DWARFS         |
| SUSAN       | LOATHING LEGALLY            |
| SUSAN       | LUCK OPUS                   |
| SUSAN       | MADNESS ATTACKS             |
| SUSAN       | NONE SPIKING                |
| SUSAN       | PACIFIC AMISTAD             |
| SUSAN       | SISTER FREDDY               |
| SUSAN       | TROJAN TOMORROW             |
| SUSAN       | WASH HEAVENLY               |
| SUSAN       | WORDS HUNTER                |
| CAMERON     | BEAUTY GREASE               |
| CAMERON     | BLACKOUT PRIVATE            |
| CAMERON     | BRIGHT ENCOUNTERS           |
| CAMERON     | CLUELESS BUCKET             |
| CAMERON     | CONQUERER NUTS              |
| CAMERON     | CROW GREASE                 |
| CAMERON     | FLOATS GARDEN               |
| CAMERON     | GLADIATOR WESTWARD          |
| CAMERON     | GRIT CLOCKWORK              |
| CAMERON     | HARRY IDAHO                 |
| CAMERON     | HAWK CHILL                  |
| CAMERON     | HELLFIGHTERS SIERRA         |
| CAMERON     | JADE BUNCH                  |
| CAMERON     | JUGGLER HARDLY              |
| CAMERON     | LAMBS CINCINATTI            |
| CAMERON     | MALLRATS UNITED             |
| CAMERON     | MOVIE SHAKESPEARE           |
| CAMERON     | MURDER ANTITRUST            |
| CAMERON     | ORIENT CLOSER               |
| CAMERON     | PEARL DESTINY               |
| CAMERON     | PILOT HOOSIERS              |
| CAMERON     | PINOCCHIO SIMON             |
| CAMERON     | PRIVATE DROP                |
| CAMERON     | RIGHT CRANES                |
| CAMERON     | RINGS HEARTBREAKERS         |
| CAMERON     | ROCK INSTINCT               |
| CAMERON     | ROOTS REMEMBER              |
| CAMERON     | SECRETARY ROUGE             |
| CAMERON     | STOCK GLASS                 |
| CAMERON     | TOMATOES HELLFIGHTERS       |
| CAMERON     | TYCOON GATHERING            |
| CAMERON     | WASTELAND DIVINE            |
| CAMERON     | WIFE TURN                   |
| RUSSELL     | ARABIA DOGMA                |
| RUSSELL     | ARIZONA BANG                |
| RUSSELL     | CINCINATTI WHISPERER        |
| RUSSELL     | CONFESSIONS MAGUIRE         |
| RUSSELL     | CRAZY HOME                  |
| RUSSELL     | DINOSAUR SECRETARY          |
| RUSSELL     | FIDDLER LOST                |
| RUSSELL     | FLATLINERS KILLER           |
| RUSSELL     | HURRICANE AFFAIR            |
| RUSSELL     | IDOLS SNATCHERS             |
| RUSSELL     | MATRIX SNOWMAN              |
| RUSSELL     | MOVIE SHAKESPEARE           |
| RUSSELL     | MUMMY CREATURES             |
| RUSSELL     | PANKY SUBMARINE             |
| RUSSELL     | PAYCHECK WAIT               |
| RUSSELL     | PRIX UNDEFEATED             |
| RUSSELL     | REUNION WITCHES             |
| RUSSELL     | SEA VIRGIN                  |
| RUSSELL     | SIERRA DIVIDE               |
| RUSSELL     | SOLDIERS EVOLUTION          |
| RUSSELL     | SPINAL ROCKY                |
| RUSSELL     | STREETCAR INTENTIONS        |
| RUSSELL     | SUNRISE LEAGUE              |
| RUSSELL     | SUSPECTS QUILLS             |
| RUSSELL     | WORKER TARZAN               |
| MORGAN      | ARACHNOPHOBIA ROLLERCOASTER |
| MORGAN      | BOILED DARES                |
| MORGAN      | CANDIDATE PERDITION         |
| MORGAN      | CONTACT ANONYMOUS           |
| MORGAN      | DECEIVER BETRAYED           |
| MORGAN      | DRACULA CRYSTAL             |
| MORGAN      | DRUMS DYNAMITE              |
| MORGAN      | EXCITEMENT EVE              |
| MORGAN      | FLATLINERS KILLER           |
| MORGAN      | GENTLEMEN STAGE             |
| MORGAN      | HARRY IDAHO                 |
| MORGAN      | LOATHING LEGALLY            |
| MORGAN      | ORDER BETRAYED              |
| MORGAN      | PAPI NECKLACE               |
| MORGAN      | PET HAUNTING                |
| MORGAN      | PINOCCHIO SIMON             |
| MORGAN      | PRIX UNDEFEATED             |
| MORGAN      | RECORDS ZORRO               |
| MORGAN      | REIGN GENTLEMEN             |
| MORGAN      | RESERVOIR ADAPTATION        |
| MORGAN      | RINGS HEARTBREAKERS         |
| MORGAN      | RUGRATS SHAKESPEARE         |
| MORGAN      | STAGECOACH ARMAGEDDON       |
| MORGAN      | TIGHTS DAWN                 |
| MORGAN      | UNCUT SUICIDES              |
| MORGAN      | WEST LION                   |
| MORGAN      | WOLVES DESIRE               |
| MORGAN      | ALI FOREVER                 |
| MORGAN      | BETRAYED REAR               |
| MORGAN      | BOULEVARD MOB               |
| MORGAN      | CLUELESS BUCKET             |
| MORGAN      | CRAZY HOME                  |
| MORGAN      | CROW GREASE                 |
| MORGAN      | DARKO DORADO                |
| MORGAN      | DIVORCE SHINING             |
| MORGAN      | DRIVER ANNIE                |
| MORGAN      | FATAL HAUNTED               |
| MORGAN      | FROGMEN BREAKING            |
| MORGAN      | HOLES BRANNIGAN             |
| MORGAN      | HOLY TADPOLE                |
| MORGAN      | ILLUSION AMELIE             |
| MORGAN      | LOVERBOY ATTACKS            |
| MORGAN      | NEIGHBORS CHARADE           |
| MORGAN      | SAGEBRUSH CLUELESS          |
| MORGAN      | SLEUTH ORIENT               |
| MORGAN      | SPICE SORORITY              |
| MORGAN      | STAR OPERATION              |
| MORGAN      | SUIT WALLS                  |
| MORGAN      | SUNSET RACER                |
| MORGAN      | TROOPERS METAL              |
| MORGAN      | WASH HEAVENLY               |
| MORGAN      | WRONG BEHAVIOR              |
| HARRISON    | BADMAN DAWN                 |
| HARRISON    | BALLROOM MOCKINGBIRD        |
| HARRISON    | DOUBLE WRATH                |
| HARRISON    | DOUBTFIRE LABYRINTH         |
| HARRISON    | ELEPHANT TROJAN             |
| HARRISON    | FANTASIA PARK               |
| HARRISON    | GREEDY ROOTS                |
| HARRISON    | GROOVE FICTION              |
| HARRISON    | HALF OUTFIELD               |
| HARRISON    | HOMICIDE PEACH              |
| HARRISON    | LADY STAGE                  |
| HARRISON    | LOSE INCH                   |
| HARRISON    | MUPPET MILE                 |
| HARRISON    | NASH CHOCOLAT               |
| HARRISON    | PAST SUICIDES               |
| HARRISON    | PERDITION FARGO             |
| HARRISON    | PLUTO OLEANDER              |
| HARRISON    | PUNK DIVORCE                |
| HARRISON    | RANDOM GO                   |
| HARRISON    | ROLLERCOASTER BRINGING      |
| HARRISON    | RUSHMORE MERMAID            |
| HARRISON    | STING PERSONAL              |
| HARRISON    | THIEF PELICAN               |
| HARRISON    | WAGON JAWS                  |
| HARRISON    | WALLS ARTIST                |
| HARRISON    | WEDDING APOLLO              |
| HARRISON    | WONDERLAND CHRISTMAS        |
| HARRISON    | WYOMING STORM               |
| DAN         | ARGONAUTS TOWN              |
| DAN         | BACKLASH UNDEFEATED         |
| DAN         | BORN SPINAL                 |
| DAN         | BOULEVARD MOB               |
| DAN         | BULL SHAWSHANK              |
| DAN         | CATCH AMISTAD               |
| DAN         | FRENCH HOLIDAY              |
| DAN         | FRISCO FORREST              |
| DAN         | GROSSE WONDERFUL            |
| DAN         | HEAVYWEIGHTS BEAST          |
| DAN         | HOLES BRANNIGAN             |
| DAN         | IGBY MAKER                  |
| DAN         | JEKYLL FROGMEN              |
| DAN         | JUNGLE CLOSER               |
| DAN         | MIXED DOORS                 |
| DAN         | MUMMY CREATURES             |
| DAN         | NEWSIES STORY               |
| DAN         | OUTFIELD MASSACRE           |
| DAN         | PANIC CLUB                  |
| DAN         | ROOF CHAMPION               |
| DAN         | SHANGHAI TYCOON             |
| DAN         | STEERS ARMAGEDDON           |
| DAN         | VERTIGO NORTHWEST           |
| DAN         | WANDA CHAMBER               |
| RENEE       | ALADDIN CALENDAR            |
| RENEE       | ALIEN CENTER                |
| RENEE       | ARTIST COLDBLOODED          |
| RENEE       | COMA HEAD                   |
| RENEE       | CONNECTION MICROCOSMOS      |
| RENEE       | CREEPERS KANE               |
| RENEE       | CRUSADE HONEY               |
| RENEE       | DESPERATE TRAINSPOTTING     |
| RENEE       | DOUBTFIRE LABYRINTH         |
| RENEE       | EFFECT GLADIATOR            |
| RENEE       | EYES DRIVING                |
| RENEE       | FIRE WOLVES                 |
| RENEE       | FRIDA SLIPPER               |
| RENEE       | HANDICAP BOONDOCK           |
| RENEE       | HOLLYWOOD ANONYMOUS         |
| RENEE       | HOPE TOOTSIE                |
| RENEE       | INFORMER DOUBLE             |
| RENEE       | INVASION CYCLONE            |
| RENEE       | MAGUIRE APACHE              |
| RENEE       | MILLION ACE                 |
| RENEE       | QUEST MUSSOLINI             |
| RENEE       | RAGE GAMES                  |
| RENEE       | ROCKETEER MOTHER            |
| RENEE       | ROCKY WAR                   |
| RENEE       | SECRETS PARADISE            |
| RENEE       | SHANE DARKNESS              |
| RENEE       | SHAWSHANK BUBBLE            |
| RENEE       | SILENCE KANE                |
| RENEE       | SMOKING BARBARELLA          |
| RENEE       | SPIRITED CASUALTIES         |
| RENEE       | SUNDANCE INVASION           |
| RENEE       | THIEF PELICAN               |
| RENEE       | UNTOUCHABLES SUNRISE        |
| CUBA        | ARACHNOPHOBIA ROLLERCOASTER |
| CUBA        | ARMAGEDDON LOST             |
| CUBA        | ARSENIC INDEPENDENCE        |
| CUBA        | BADMAN DAWN                 |
| CUBA        | BARBARELLA STREETCAR        |
| CUBA        | CHAPLIN LICENSE             |
| CUBA        | CHICAGO NORTH               |
| CUBA        | CINCINATTI WHISPERER        |
| CUBA        | FICTION CHRISTMAS           |
| CUBA        | GROSSE WONDERFUL            |
| CUBA        | HAPPINESS UNITED            |
| CUBA        | KING EVOLUTION              |
| CUBA        | LESSON CLEOPATRA            |
| CUBA        | MAKER GABLES                |
| CUBA        | MANNEQUIN WORST             |
| CUBA        | METROPOLIS COMA             |
| CUBA        | ORANGE GRAPES               |
| CUBA        | PAPI NECKLACE               |
| CUBA        | PRESIDENT BANG              |
| CUBA        | ROBBERS JOON                |
| CUBA        | SHIP WONDERLAND             |
| CUBA        | STRANGELOVE DESIRE          |
| CUBA        | VELVET TERMINATOR           |
| CUBA        | WAR NOTTING                 |
| CUBA        | WEST LION                   |
| WARREN      | AMERICAN CIRCUS             |
| WARREN      | BADMAN DAWN                 |
| WARREN      | BEETHOVEN EXORCIST          |
| WARREN      | BOONDOCK BALLROOM           |
| WARREN      | CHILL LUCK                  |
| WARREN      | COMMANDMENTS EXPRESS        |
| WARREN      | CONEHEADS SMOOCHY           |
| WARREN      | CONFESSIONS MAGUIRE         |
| WARREN      | GRINCH MASSAGE              |
| WARREN      | HAMLET WISDOM               |
| WARREN      | HEAVYWEIGHTS BEAST          |
| WARREN      | HOBBIT ALIEN                |
| WARREN      | IMPACT ALADDIN              |
| WARREN      | LANGUAGE COWBOY             |
| WARREN      | LIES TREATMENT              |
| WARREN      | MEET CHOCOLATE              |
| WARREN      | MERMAID INSECTS             |
| WARREN      | MONSTER SPARTACUS           |
| WARREN      | NAME DETECTIVE              |
| WARREN      | OLEANDER CLUE               |
| WARREN      | OZ LIAISONS                 |
| WARREN      | POTTER CONNECTICUT          |
| WARREN      | ROCKETEER MOTHER            |
| WARREN      | RUNAWAY TENENBAUMS          |
| WARREN      | SHAKESPEARE SADDLE          |
| WARREN      | SHEPHERD MIDSUMMER          |
| WARREN      | SHIP WONDERLAND             |
| WARREN      | SKY MIRACLE                 |
| WARREN      | SUBMARINE BED               |
| WARREN      | SUPERFLY TRIP               |
| WARREN      | TOWN ARK                    |
| WARREN      | VERTIGO NORTHWEST           |
| PENELOPE    | BASIC EASY                  |
| PENELOPE    | BEDAZZLED MARRIED           |
| PENELOPE    | CHINATOWN GLADIATOR         |
| PENELOPE    | CHRISTMAS MOONSHINE         |
| PENELOPE    | DARES PLUTO                 |
| PENELOPE    | DINOSAUR SECRETARY          |
| PENELOPE    | DOCTOR GRAIL                |
| PENELOPE    | DRIVING POLISH              |
| PENELOPE    | HELLFIGHTERS SIERRA         |
| PENELOPE    | HOLOCAUST HIGHBALL          |
| PENELOPE    | JUGGLER HARDLY              |
| PENELOPE    | LEATHERNECKS DWARFS         |
| PENELOPE    | MONEY HAROLD                |
| PENELOPE    | ORANGE GRAPES               |
| PENELOPE    | ORDER BETRAYED              |
| PENELOPE    | PARK CITIZEN                |
| PENELOPE    | PITTSBURGH HUNCHBACK        |
| PENELOPE    | POSEIDON FOREVER            |
| PENELOPE    | RANGE MOONWALKER            |
| PENELOPE    | REAR TRADING                |
| PENELOPE    | REEF SALUTE                 |
| PENELOPE    | ROUGE SQUAD                 |
| PENELOPE    | SPIRIT FLINTSTONES          |
| PENELOPE    | TOMATOES HELLFIGHTERS       |
| PENELOPE    | TOURIST PELICAN             |
| PENELOPE    | TRIP NEWTON                 |
| PENELOPE    | WYOMING STORM               |
| LIZA        | CHICAGO NORTH               |
| LIZA        | CLASH FREDDY                |
| LIZA        | CLUE GRAIL                  |
| LIZA        | COMMAND DARLING             |
| LIZA        | CRAFT OUTFIELD              |
| LIZA        | CRYSTAL BREAKING            |
| LIZA        | DEER VIRGINIAN              |
| LIZA        | DESERT POSEIDON             |
| LIZA        | ENEMY ODDS                  |
| LIZA        | EXTRAORDINARY CONQUERER     |
| LIZA        | FRISCO FORREST              |
| LIZA        | GENTLEMEN STAGE             |
| LIZA        | IDENTITY LOVER              |
| LIZA        | JEDI BENEATH                |
| LIZA        | LESSON CLEOPATRA            |
| LIZA        | OCTOBER SUBMARINE           |
| LIZA        | PANKY SUBMARINE             |
| LIZA        | PARIS WEEKEND               |
| LIZA        | PAYCHECK WAIT               |
| LIZA        | SCORPION APOLLO             |
| LIZA        | SENSIBILITY REAR            |
| LIZA        | STOCK GLASS                 |
| LIZA        | TERMINATOR CLUB             |
| LIZA        | TEXAS WATCH                 |
| LIZA        | WEDDING APOLLO              |
| SALMA       | AMISTAD MIDSUMMER           |
| SALMA       | ANTITRUST TOMATOES          |
| SALMA       | BIRDCAGE CASPER             |
| SALMA       | BLUES INSTINCT              |
| SALMA       | CLOCKWORK PARADISE          |
| SALMA       | CLONES PINOCCHIO            |
| SALMA       | COLOR PHILADELPHIA          |
| SALMA       | DETAILS PACKER              |
| SALMA       | DOCTOR GRAIL                |
| SALMA       | FALCON VOLUME               |
| SALMA       | FELLOWSHIP AUTUMN           |
| SALMA       | GO PURPLE                   |
| SALMA       | ISHTAR ROCKETEER            |
| SALMA       | JUGGLER HARDLY              |
| SALMA       | JUMPING WRATH               |
| SALMA       | LUST LOCK                   |
| SALMA       | NEMO CAMPUS                 |
| SALMA       | OZ LIAISONS                 |
| SALMA       | PANKY SUBMARINE             |
| SALMA       | PERSONAL LADYBUGS           |
| SALMA       | REBEL AIRPORT               |
| SALMA       | SIEGE MADRE                 |
| SALMA       | WAR NOTTING                 |
| SALMA       | WASH HEAVENLY               |
| SALMA       | ZHIVAGO CORE                |
| JULIANNE    | ADAPTATION HOLES            |
| JULIANNE    | ATLANTIS CAUSE              |
| JULIANNE    | BERETS AGENT                |
| JULIANNE    | BULL SHAWSHANK              |
| JULIANNE    | CHOCOLATE DUCK              |
| JULIANNE    | CINCINATTI WHISPERER        |
| JULIANNE    | COWBOY DOOM                 |
| JULIANNE    | DESIRE ALIEN                |
| JULIANNE    | DISTURBING SCARFACE         |
| JULIANNE    | DOUBLE WRATH                |
| JULIANNE    | DOUBTFIRE LABYRINTH         |
| JULIANNE    | DYNAMITE TARZAN             |
| JULIANNE    | ENOUGH RAGING               |
| JULIANNE    | HONEY TIES                  |
| JULIANNE    | HUNTING MUSKETEERS          |
| JULIANNE    | HYSTERICAL GRAIL            |
| JULIANNE    | JEDI BENEATH                |
| JULIANNE    | JEEPERS WEDDING             |
| JULIANNE    | KARATE MOON                 |
| JULIANNE    | KRAMER CHOCOLATE            |
| JULIANNE    | LORD ARIZONA                |
| JULIANNE    | MIGHTY LUCK                 |
| JULIANNE    | MILE MULAN                  |
| JULIANNE    | MODERN DORADO               |
| JULIANNE    | MONTEREY LABYRINTH          |
| JULIANNE    | REQUIEM TYCOON              |
| JULIANNE    | RIDGEMONT SUBMARINE         |
| JULIANNE    | SHEPHERD MIDSUMMER          |
| JULIANNE    | SUICIDES SILENCE            |
| JULIANNE    | TITANIC BOONDOCK            |
| JULIANNE    | UNTOUCHABLES SUNRISE        |
| JULIANNE    | WORKER TARZAN               |
| SCARLETT    | AMISTAD MIDSUMMER           |
| SCARLETT    | BEETHOVEN EXORCIST          |
| SCARLETT    | BULWORTH COMMANDMENTS       |
| SCARLETT    | CALIFORNIA BIRDS            |
| SCARLETT    | CREEPERS KANE               |
| SCARLETT    | DOUBTFIRE LABYRINTH         |
| SCARLETT    | DUDE BLINDNESS              |
| SCARLETT    | DURHAM PANKY                |
| SCARLETT    | EVE RESURRECTION            |
| SCARLETT    | FEATHERS METAL              |
| SCARLETT    | FIDDLER LOST                |
| SCARLETT    | FLATLINERS KILLER           |
| SCARLETT    | FULL FLATLINERS             |
| SCARLETT    | IDENTITY LOVER              |
| SCARLETT    | INVASION CYCLONE            |
| SCARLETT    | LUCK OPUS                   |
| SCARLETT    | MOULIN WAKE                 |
| SCARLETT    | RESERVOIR ADAPTATION        |
| SCARLETT    | ROOF CHAMPION               |
| SCARLETT    | SEATTLE EXPECATIONS         |
| SCARLETT    | SHAWSHANK BUBBLE            |
| SCARLETT    | SNATCH SLIPPER              |
| SCARLETT    | SUBMARINE BED               |
| SCARLETT    | TENENBAUMS COMMAND          |
| SCARLETT    | WORDS HUNTER                |
| SCARLETT    | YOUTH KICK                  |
| ALBERT      | BED HIGHBALL                |
| ALBERT      | BRIGHT ENCOUNTERS           |
| ALBERT      | BROOKLYN DESERT             |
| ALBERT      | CAMELOT VACATION            |
| ALBERT      | CONFUSED CANDLES            |
| ALBERT      | CRAZY HOME                  |
| ALBERT      | DALMATIONS SWEDEN           |
| ALBERT      | DOCTOR GRAIL                |
| ALBERT      | DRAGON SQUAD                |
| ALBERT      | FLINTSTONES HAPPINESS       |
| ALBERT      | FRISCO FORREST              |
| ALBERT      | GLEAMING JAWBREAKER         |
| ALBERT      | GOLDMINE TYCOON             |
| ALBERT      | HANDICAP BOONDOCK           |
| ALBERT      | HELLFIGHTERS SIERRA         |
| ALBERT      | HOMICIDE PEACH              |
| ALBERT      | HONEY TIES                  |
| ALBERT      | IDOLS SNATCHERS             |
| ALBERT      | KILL BROTHERHOOD            |
| ALBERT      | MANCHURIAN CURTAIN          |
| ALBERT      | MEMENTO ZOOLANDER           |
| ALBERT      | MIXED DOORS                 |
| ALBERT      | MOURNING PURPLE             |
| ALBERT      | NEWTON LABYRINTH            |
| ALBERT      | PATRIOT ROMAN               |
| ALBERT      | PITY BOUND                  |
| ALBERT      | RAGE GAMES                  |
| ALBERT      | TAXI KICK                   |
| ALBERT      | TRAP GUYS                   |
| ALBERT      | VOLCANO TEXAS               |
| ALBERT      | WATERSHIP FRONTIER          |
| FRANCES     | AMERICAN CIRCUS             |
| FRANCES     | ARABIA DOGMA                |
| FRANCES     | ATLANTIS CAUSE              |
| FRANCES     | BEACH HEARTBREAKERS         |
| FRANCES     | BONNIE HOLOCAUST            |
| FRANCES     | BREAKING HOME               |
| FRANCES     | CROSSROADS CASUALTIES       |
| FRANCES     | CROW GREASE                 |
| FRANCES     | CUPBOARD SINNERS            |
| FRANCES     | DROP WATERFRONT             |
| FRANCES     | DURHAM PANKY                |
| FRANCES     | ESCAPE METROPOLIS           |
| FRANCES     | FIREBALL PHILADELPHIA       |
| FRANCES     | GAMES BOWFINGER             |
| FRANCES     | GOODFELLAS SALUTE           |
| FRANCES     | GORGEOUS BINGO              |
| FRANCES     | HOCUS FRIDA                 |
| FRANCES     | INVASION CYCLONE            |
| FRANCES     | IRON MOON                   |
| FRANCES     | MADNESS ATTACKS             |
| FRANCES     | PLATOON INSTINCT            |
| FRANCES     | SQUAD FISH                  |
| FRANCES     | SUICIDES SILENCE            |
| KEVIN       | ARGONAUTS TOWN              |
| KEVIN       | BABY HALL                   |
| KEVIN       | BACKLASH UNDEFEATED         |
| KEVIN       | BLADE POLISH                |
| KEVIN       | CAPER MOTIONS               |
| KEVIN       | CHICAGO NORTH               |
| KEVIN       | CLOCKWORK PARADISE          |
| KEVIN       | DADDY PITTSBURGH            |
| KEVIN       | ENOUGH RAGING               |
| KEVIN       | FREAKY POCUS                |
| KEVIN       | GHOST GROUNDHOG             |
| KEVIN       | GOLDFINGER SENSIBILITY      |
| KEVIN       | GRIT CLOCKWORK              |
| KEVIN       | GUNFIGHT MOON               |
| KEVIN       | HEAVENLY GUN                |
| KEVIN       | INFORMER DOUBLE             |
| KEVIN       | MAKER GABLES                |
| KEVIN       | MICROCOSMOS PARADISE        |
| KEVIN       | MYSTIC TRUMAN               |
| KEVIN       | NATURAL STOCK               |
| KEVIN       | ORANGE GRAPES               |
| KEVIN       | RAGE GAMES                  |
| KEVIN       | RESURRECTION SILVERADO      |
| KEVIN       | RULES HUMAN                 |
| KEVIN       | SATISFACTION CONFIDENTIAL   |
| KEVIN       | SCORPION APOLLO             |
| KEVIN       | SHOW LORD                   |
| KEVIN       | SONG HEDWIG                 |
| KEVIN       | STALLION SUNDANCE           |
| KEVIN       | STING PERSONAL              |
| KEVIN       | TRIP NEWTON                 |
| KEVIN       | WAIT CIDER                  |
| KEVIN       | WESTWARD SEABISCUIT         |
| CATE        | ANNIE IDENTITY              |
| CATE        | BLOOD ARGONAUTS             |
| CATE        | CAPER MOTIONS               |
| CATE        | COMANCHEROS ENEMY           |
| CATE        | DARN FORRESTER              |
| CATE        | DOCTOR GRAIL                |
| CATE        | FACTORY DRAGON              |
| CATE        | FIDDLER LOST                |
| CATE        | FLYING HOOK                 |
| CATE        | FRENCH HOLIDAY              |
| CATE        | GABLES METROPOLIS           |
| CATE        | HAWK CHILL                  |
| CATE        | INSIDER ARIZONA             |
| CATE        | JERSEY SASSY                |
| CATE        | LEGEND JEDI                 |
| CATE        | MASSAGE IMAGE               |
| CATE        | NAME DETECTIVE              |
| CATE        | PACIFIC AMISTAD             |
| CATE        | PATTON INTERVIEW            |
| CATE        | PERDITION FARGO             |
| CATE        | POTTER CONNECTICUT          |
| CATE        | PRIDE ALAMO                 |
| CATE        | SALUTE APOLLO               |
| CATE        | SEARCHERS WAIT              |
| CATE        | SNATCH SLIPPER              |
| CATE        | TOWERS HURRICANE            |
| CATE        | TROJAN TOMORROW             |
| CATE        | VIRGIN DAISY                |
| CATE        | VOLCANO TEXAS               |
| CATE        | WATERSHIP FRONTIER          |
| DARYL       | BAREFOOT MANCHURIAN         |
| DARYL       | BORROWERS BEDAZZLED         |
| DARYL       | BROTHERHOOD BLANKET         |
| DARYL       | COLOR PHILADELPHIA          |
| DARYL       | DADDY PITTSBURGH            |
| DARYL       | DIARY PANIC                 |
| DARYL       | DOWNHILL ENOUGH             |
| DARYL       | DRACULA CRYSTAL             |
| DARYL       | GANDHI KWAI                 |
| DARYL       | GOLDMINE TYCOON             |
| DARYL       | HALF OUTFIELD               |
| DARYL       | HOBBIT ALIEN                |
| DARYL       | HOOSIERS BIRDCAGE           |
| DARYL       | ILLUSION AMELIE             |
| DARYL       | ISLAND EXORCIST             |
| DARYL       | LICENSE WEEKEND             |
| DARYL       | MOONWALKER FOOL             |
| DARYL       | MOURNING PURPLE             |
| DARYL       | OPUS ICE                    |
| DARYL       | PEARL DESTINY               |
| DARYL       | PIZZA JUMANJI               |
| DARYL       | PURPLE MOVIE                |
| DARYL       | SLEEPLESS MONSOON           |
| DARYL       | SPEED SUIT                  |
| DARYL       | SPOILERS HELLFIGHTERS       |
| DARYL       | STRICTLY SCARFACE           |
| DARYL       | TREATMENT JEKYLL            |
| DARYL       | UNBREAKABLE KARATE          |
| DARYL       | VELVET TERMINATOR           |
| DARYL       | WASTELAND DIVINE            |
| GRETA       | ALABAMA DEVIL               |
| GRETA       | ANNIE IDENTITY              |
| GRETA       | ARIZONA BANG                |
| GRETA       | ATLANTIS CAUSE              |
| GRETA       | BADMAN DAWN                 |
| GRETA       | BASIC EASY                  |
| GRETA       | BUNCH MINDS                 |
| GRETA       | CALENDAR GUNFIGHT           |
| GRETA       | DARES PLUTO                 |
| GRETA       | FLYING HOOK                 |
| GRETA       | GRAIL FRANKENSTEIN          |
| GRETA       | HIGHBALL POTTER             |
| GRETA       | HOOSIERS BIRDCAGE           |
| GRETA       | ILLUSION AMELIE             |
| GRETA       | IMAGE PRINCESS              |
| GRETA       | JAWS HARRY                  |
| GRETA       | LADYBUGS ARMAGEDDON         |
| GRETA       | LOATHING LEGALLY            |
| GRETA       | MAGNOLIA FORRESTER          |
| GRETA       | MONSTER SPARTACUS           |
| GRETA       | PULP BEVERLY                |
| GRETA       | REQUIEM TYCOON              |
| GRETA       | SATURDAY LAMBS              |
| GRETA       | SLIPPER FIDELITY            |
| GRETA       | SUSPECTS QUILLS             |
| GRETA       | VACATION BOONDOCK           |
| GRETA       | WOLVES DESIRE               |
| JANE        | BACKLASH UNDEFEATED         |
| JANE        | BENEATH RUSH                |
| JANE        | BRAVEHEART HUMAN            |
| JANE        | CARIBBEAN LIBERTY           |
| JANE        | CHOCOLAT HARRY              |
| JANE        | DANCING FEVER               |
| JANE        | FLAMINGOS CONNECTICUT       |
| JANE        | GROOVE FICTION              |
| JANE        | HOPE TOOTSIE                |
| JANE        | HOURS RAGE                  |
| JANE        | IDOLS SNATCHERS             |
| JANE        | JEDI BENEATH                |
| JANE        | KARATE MOON                 |
| JANE        | LEGALLY SECRETARY           |
| JANE        | LUCK OPUS                   |
| JANE        | MONEY HAROLD                |
| JANE        | OUTFIELD MASSACRE           |
| JANE        | POTTER CONNECTICUT          |
| JANE        | RAINBOW SHOCK               |
| JANE        | SCISSORHANDS SLUMS          |
| JANE        | SILVERADO GOLDFINGER        |
| JANE        | SLIPPER FIDELITY            |
| JANE        | TALENTED HOMICIDE           |
| JANE        | TEMPLE ATTRACTION           |
| JANE        | UNCUT SUICIDES              |
| ADAM        | BLINDNESS GUN               |
| ADAM        | BLOOD ARGONAUTS             |
| ADAM        | CHAMBER ITALIAN             |
| ADAM        | CLERKS ANGELS               |
| ADAM        | CLUELESS BUCKET             |
| ADAM        | FICTION CHRISTMAS           |
| ADAM        | GABLES METROPOLIS           |
| ADAM        | GREASE YOUTH                |
| ADAM        | HEAVEN FREEDOM              |
| ADAM        | LOVERBOY ATTACKS            |
| ADAM        | MASKED BUBBLE               |
| ADAM        | MOCKINGBIRD HOLLYWOOD       |
| ADAM        | NOON PAPI                   |
| ADAM        | OPEN AFRICAN                |
| ADAM        | PRINCESS GIANT              |
| ADAM        | SADDLE ANTITRUST            |
| ADAM        | SLEEPY JAPANESE             |
| ADAM        | TORQUE BOUND                |
| ADAM        | TOWERS HURRICANE            |
| ADAM        | TRAIN BUNCH                 |
| ADAM        | VACATION BOONDOCK           |
| ADAM        | WORDS HUNTER                |
| RICHARD     | AIRPLANE SIERRA             |
| RICHARD     | BALLOON HOMEWARD            |
| RICHARD     | CHAMBER ITALIAN             |
| RICHARD     | CONEHEADS SMOOCHY           |
| RICHARD     | DARKO DORADO                |
| RICHARD     | EARTH VISION                |
| RICHARD     | EMPIRE MALKOVICH            |
| RICHARD     | ENOUGH RAGING               |
| RICHARD     | FRISCO FORREST              |
| RICHARD     | FUGITIVE MAGUIRE            |
| RICHARD     | GASLIGHT CRUSADE            |
| RICHARD     | GONE TROUBLE                |
| RICHARD     | GROUNDHOG UNCUT             |
| RICHARD     | GUYS FALCON                 |
| RICHARD     | HANKY OCTOBER               |
| RICHARD     | HEAVEN FREEDOM              |
| RICHARD     | ILLUSION AMELIE             |
| RICHARD     | INSTINCT AIRPORT            |
| RICHARD     | LEBOWSKI SOLDIERS           |
| RICHARD     | MODEL FISH                  |
| RICHARD     | MONTEZUMA COMMAND           |
| RICHARD     | OKLAHOMA JUMANJI            |
| RICHARD     | PAJAMA JAWBREAKER           |
| RICHARD     | RESURRECTION SILVERADO      |
| RICHARD     | SLEEPY JAPANESE             |
| RICHARD     | SUPERFLY TRIP               |
| RICHARD     | TENENBAUMS COMMAND          |
| RICHARD     | TOMATOES HELLFIGHTERS       |
| RICHARD     | VAMPIRE WHALE               |
| RICHARD     | WAGON JAWS                  |
| GENE        | CHAINSAW UPTOWN             |
| GENE        | CHISUM BEHAVIOR             |
| GENE        | CLUE GRAIL                  |
| GENE        | DEEP CRUSADE                |
| GENE        | DOORS PRESIDENT             |
| GENE        | DRAGON SQUAD                |
| GENE        | ELF MURDER                  |
| GENE        | FROST HEAD                  |
| GENE        | GUMP DATE                   |
| GENE        | HEDWIG ALTER                |
| GENE        | MANNEQUIN WORST             |
| GENE        | MODEL FISH                  |
| GENE        | NIGHTMARE CHILL             |
| GENE        | PANTHER REDS                |
| GENE        | PITY BOUND                  |
| GENE        | POND SEATTLE                |
| GENE        | SUIT WALLS                  |
| GENE        | TOOTSIE PILOT               |
| GENE        | TORQUE BOUND                |
| GENE        | TRUMAN CRAZY                |
| GENE        | UPRISING UPTOWN             |
| GENE        | VANISHING ROCKY             |
| RITA        | ARACHNOPHOBIA ROLLERCOASTER |
| RITA        | ARSENIC INDEPENDENCE        |
| RITA        | BEHAVIOR RUNAWAY            |
| RITA        | BORN SPINAL                 |
| RITA        | COMMAND DARLING             |
| RITA        | EARRING INSTINCT            |
| RITA        | FLAMINGOS CONNECTICUT       |
| RITA        | GENTLEMEN STAGE             |
| RITA        | GILBERT PELICAN             |
| RITA        | GODFATHER DIARY             |
| RITA        | IMPOSSIBLE PREJUDICE        |
| RITA        | INDIAN LOVE                 |
| RITA        | JERK PAYCHECK               |
| RITA        | LUKE MUMMY                  |
| RITA        | MAKER GABLES                |
| RITA        | NATIONAL STORY              |
| RITA        | NORTHWEST POLISH            |
| RITA        | RECORDS ZORRO               |
| RITA        | SNATCH SLIPPER              |
| RITA        | TRAINSPOTTING STRANGERS     |
| ED          | AMELIE HELLFIGHTERS         |
| ED          | ANGELS LIFE                 |
| ED          | APOLLO TEEN                 |
| ED          | BAREFOOT MANCHURIAN         |
| ED          | BEAUTY GREASE               |
| ED          | CROSSROADS CASUALTIES       |
| ED          | DAUGHTER MADIGAN            |
| ED          | DEVIL DESIRE                |
| ED          | DOORS PRESIDENT             |
| ED          | DROP WATERFRONT             |
| ED          | DUMBO LUST                  |
| ED          | EASY GLADIATOR              |
| ED          | ESCAPE METROPOLIS           |
| ED          | FALCON VOLUME               |
| ED          | GODFATHER DIARY             |
| ED          | HAROLD FRENCH               |
| ED          | HELLFIGHTERS SIERRA         |
| ED          | HOLES BRANNIGAN             |
| ED          | JADE BUNCH                  |
| ED          | JERSEY SASSY                |
| ED          | LUST LOCK                   |
| ED          | MAJESTIC FLOATS             |
| ED          | NEMO CAMPUS                 |
| ED          | OZ LIAISONS                 |
| ED          | PLUTO OLEANDER              |
| ED          | SEVEN SWARM                 |
| ED          | SLEEPY JAPANESE             |
| ED          | SLING LUKE                  |
| ED          | SOMETHING DUCK              |
| ED          | STATE WASTELAND             |
| ED          | VAMPIRE WHALE               |
| ED          | WRONG BEHAVIOR              |
| MORGAN      | AGENT TRUMAN                |
| MORGAN      | ALICE FANTASIA              |
| MORGAN      | BAREFOOT MANCHURIAN         |
| MORGAN      | BREAKING HOME               |
| MORGAN      | CLUB GRAFFITI               |
| MORGAN      | DESPERATE TRAINSPOTTING     |
| MORGAN      | DRACULA CRYSTAL             |
| MORGAN      | DRIVER ANNIE                |
| MORGAN      | DURHAM PANKY                |
| MORGAN      | EARLY HOME                  |
| MORGAN      | FARGO GANDHI                |
| MORGAN      | GUYS FALCON                 |
| MORGAN      | HEAVEN FREEDOM              |
| MORGAN      | HORN WORKING                |
| MORGAN      | HYSTERICAL GRAIL            |
| MORGAN      | JUGGLER HARDLY              |
| MORGAN      | LORD ARIZONA                |
| MORGAN      | MASSAGE IMAGE               |
| MORGAN      | MOVIE SHAKESPEARE           |
| MORGAN      | MUSIC BOONDOCK              |
| MORGAN      | POLISH BROOKLYN             |
| MORGAN      | PUNK DIVORCE                |
| MORGAN      | ROSES TREASURE              |
| MORGAN      | SAINTS BRIDE                |
| MORGAN      | SPLASH GUMP                 |
| MORGAN      | STAR OPERATION              |
| MORGAN      | TUXEDO MILE                 |
| LUCILLE     | AIRPORT POLLOCK             |
| LUCILLE     | BALLROOM MOCKINGBIRD        |
| LUCILLE     | BEAUTY GREASE               |
| LUCILLE     | CASSIDY WYOMING             |
| LUCILLE     | CLOCKWORK PARADISE          |
| LUCILLE     | DAUGHTER MADIGAN            |
| LUCILLE     | DRUMS DYNAMITE              |
| LUCILLE     | GRAPES FURY                 |
| LUCILLE     | HARRY IDAHO                 |
| LUCILLE     | HYSTERICAL GRAIL            |
| LUCILLE     | IMAGE PRINCESS              |
| LUCILLE     | LAMBS CINCINATTI            |
| LUCILLE     | MAKER GABLES                |
| LUCILLE     | MASK PEACH                  |
| LUCILLE     | MISSION ZOOLANDER           |
| LUCILLE     | NORTH TEQUILA               |
| LUCILLE     | OPPOSITE NECKLACE           |
| LUCILLE     | PRESIDENT BANG              |
| LUCILLE     | ROXANNE REBEL               |
| LUCILLE     | TELEGRAPH VOYAGE            |
| LUCILLE     | TEXAS WATCH                 |
| LUCILLE     | UNFAITHFUL KILL             |
| LUCILLE     | WESTWARD SEABISCUIT         |
| LUCILLE     | WORKING MICROCOSMOS         |
| EWAN        | AMELIE HELLFIGHTERS         |
| EWAN        | ARACHNOPHOBIA ROLLERCOASTER |
| EWAN        | BASIC EASY                  |
| EWAN        | BIRCH ANTITRUST             |
| EWAN        | BOULEVARD MOB               |
| EWAN        | BUNCH MINDS                 |
| EWAN        | CLEOPATRA DEVIL             |
| EWAN        | COMMAND DARLING             |
| EWAN        | CONTACT ANONYMOUS           |
| EWAN        | CURTAIN VIDEOTAPE           |
| EWAN        | DEVIL DESIRE                |
| EWAN        | DISCIPLE MOTHER             |
| EWAN        | DUFFEL APOCALYPSE           |
| EWAN        | DUMBO LUST                  |
| EWAN        | DYNAMITE TARZAN             |
| EWAN        | ENCOUNTERS CURTAIN          |
| EWAN        | ENEMY ODDS                  |
| EWAN        | GRADUATE LORD               |
| EWAN        | ICE CROSSING                |
| EWAN        | JUGGLER HARDLY              |
| EWAN        | LONELY ELEPHANT             |
| EWAN        | LUCKY FLYING                |
| EWAN        | MERMAID INSECTS             |
| EWAN        | MOURNING PURPLE             |
| EWAN        | MULHOLLAND BEAST            |
| EWAN        | OLEANDER CLUE               |
| EWAN        | POSEIDON FOREVER            |
| EWAN        | QUEEN LUKE                  |
| EWAN        | RECORDS ZORRO               |
| EWAN        | ROOTS REMEMBER              |
| EWAN        | ROUGE SQUAD                 |
| EWAN        | SUMMER SCARFACE             |
| EWAN        | TITANIC BOONDOCK            |
| WHOOPI      | ANONYMOUS HUMAN             |
| WHOOPI      | BIRDS PERDITION             |
| WHOOPI      | CALENDAR GUNFIGHT           |
| WHOOPI      | CHANCE RESURRECTION         |
| WHOOPI      | COWBOY DOOM                 |
| WHOOPI      | DRUMS DYNAMITE              |
| WHOOPI      | GORGEOUS BINGO              |
| WHOOPI      | GRADUATE LORD               |
| WHOOPI      | KILLER INNOCENT             |
| WHOOPI      | LANGUAGE COWBOY             |
| WHOOPI      | MIGHTY LUCK                 |
| WHOOPI      | MOD SECRETARY               |
| WHOOPI      | MOTHER OLEANDER             |
| WHOOPI      | MURDER ANTITRUST            |
| WHOOPI      | OUTFIELD MASSACRE           |
| WHOOPI      | PATTON INTERVIEW            |
| WHOOPI      | PELICAN COMFORTS            |
| WHOOPI      | POTTER CONNECTICUT          |
| WHOOPI      | PULP BEVERLY                |
| WHOOPI      | RIDER CADDYSHACK            |
| WHOOPI      | RIDGEMONT SUBMARINE         |
| WHOOPI      | RIGHT CRANES                |
| WHOOPI      | ROBBERY BRIGHT              |
| WHOOPI      | ROOF CHAMPION               |
| WHOOPI      | SECRETS PARADISE            |
| WHOOPI      | SONS INTERVIEW              |
| WHOOPI      | SPIRIT FLINTSTONES          |
| WHOOPI      | SPY MILE                    |
| WHOOPI      | STRICTLY SCARFACE           |
| WHOOPI      | UNFAITHFUL KILL             |
| WHOOPI      | VANILLA DAY                 |
| WHOOPI      | ZOOLANDER FICTION           |
| CATE        | ATLANTIS CAUSE              |
| CATE        | BERETS AGENT                |
| CATE        | CRAZY HOME                  |
| CATE        | CROOKED FROGMEN             |
| CATE        | DANGEROUS UPTOWN            |
| CATE        | DESIRE ALIEN                |
| CATE        | FROST HEAD                  |
| CATE        | GILMORE BOILED              |
| CATE        | GREEK EVERYONE              |
| CATE        | HANDICAP BOONDOCK           |
| CATE        | INTRIGUE WORST              |
| CATE        | JUMPING WRATH               |
| CATE        | MODERN DORADO               |
| CATE        | MUPPET MILE                 |
| CATE        | PERSONAL LADYBUGS           |
| CATE        | ROLLERCOASTER BRINGING      |
| CATE        | RUNNER MADIGAN              |
| CATE        | SCARFACE BANG               |
| CATE        | SEA VIRGIN                  |
| CATE        | SHINING ROSES               |
| CATE        | SORORITY QUEEN              |
| CATE        | SPINAL ROCKY                |
| CATE        | STAMPEDE DISTURBING         |
| CATE        | STORM HAPPINESS             |
| CATE        | SUMMER SCARFACE             |
| CATE        | SUN CONFESSIONS             |
| CATE        | TREASURE COMMAND            |
| CATE        | WRATH MILE                  |
| JADA        | ALADDIN CALENDAR            |
| JADA        | ALTER VICTORY               |
| JADA        | BUNCH MINDS                 |
| JADA        | CHASING FIGHT               |
| JADA        | CRAFT OUTFIELD              |
| JADA        | CUPBOARD SINNERS            |
| JADA        | DOZEN LION                  |
| JADA        | FOREVER CANDIDATE           |
| JADA        | GARDEN ISLAND               |
| JADA        | GOSFORD DONNIE              |
| JADA        | ISHTAR ROCKETEER            |
| JADA        | JEKYLL FROGMEN              |
| JADA        | KARATE MOON                 |
| JADA        | KISSING DOLLS               |
| JADA        | KWAI HOMEWARD               |
| JADA        | LUCKY FLYING                |
| JADA        | MALKOVICH PET               |
| JADA        | MIDSUMMER GROUNDHOG         |
| JADA        | MURDER ANTITRUST            |
| JADA        | RAGE GAMES                  |
| JADA        | RAIDERS ANTITRUST           |
| JADA        | ROBBERS JOON                |
| JADA        | SALUTE APOLLO               |
| JADA        | SIDE ARK                    |
| JADA        | STATE WASTELAND             |
| JADA        | SUGAR WONKA                 |
| JADA        | SUN CONFESSIONS             |
| JADA        | TALENTED HOMICIDE           |
| JADA        | TRAMP OTHERS                |
| JADA        | TROUBLE DATE                |
| JADA        | ZOOLANDER FICTION           |
| RIVER       | BABY HALL                   |
| RIVER       | BLADE POLISH                |
| RIVER       | CHICAGO NORTH               |
| RIVER       | CONFUSED CANDLES            |
| RIVER       | DIRTY ACE                   |
| RIVER       | DOGMA FAMILY                |
| RIVER       | FIRE WOLVES                 |
| RIVER       | FROGMEN BREAKING            |
| RIVER       | GLEAMING JAWBREAKER         |
| RIVER       | GUMP DATE                   |
| RIVER       | HATE HANDICAP               |
| RIVER       | INDEPENDENCE HOTEL          |
| RIVER       | JERSEY SASSY                |
| RIVER       | KILL BROTHERHOOD            |
| RIVER       | MARS ROMAN                  |
| RIVER       | MIGHTY LUCK                 |
| RIVER       | MOVIE SHAKESPEARE           |
| RIVER       | MYSTIC TRUMAN               |
| RIVER       | PARK CITIZEN                |
| RIVER       | PARTY KNOCK                 |
| RIVER       | PINOCCHIO SIMON             |
| RIVER       | POCUS PULP                  |
| RIVER       | POND SEATTLE                |
| RIVER       | QUEEN LUKE                  |
| RIVER       | SHREK LICENSE               |
| RIVER       | SORORITY QUEEN              |
| RIVER       | SPIRIT FLINTSTONES          |
| RIVER       | SWEET BROTHERHOOD           |
| RIVER       | TEEN APOLLO                 |
| RIVER       | TRAMP OTHERS                |
| RIVER       | WARDROBE PHANTOM            |
| ANGELA      | ALTER VICTORY               |
| ANGELA      | BERETS AGENT                |
| ANGELA      | BLADE POLISH                |
| ANGELA      | BOULEVARD MOB               |
| ANGELA      | BRINGING HYSTERICAL         |
| ANGELA      | BULL SHAWSHANK              |
| ANGELA      | CASABLANCA SUPER            |
| ANGELA      | CASSIDY WYOMING             |
| ANGELA      | CAT CONEHEADS               |
| ANGELA      | CELEBRITY HORN              |
| ANGELA      | CHANCE RESURRECTION         |
| ANGELA      | COAST RAINBOW               |
| ANGELA      | CORE SUIT                   |
| ANGELA      | DAY UNFAITHFUL              |
| ANGELA      | DETECTIVE VISION            |
| ANGELA      | DUDE BLINDNESS              |
| ANGELA      | EDGE KISSING                |
| ANGELA      | EVOLUTION ALTER             |
| ANGELA      | EXORCIST STING              |
| ANGELA      | FIDDLER LOST                |
| ANGELA      | HALLOWEEN NUTS              |
| ANGELA      | HANGING DEEP                |
| ANGELA      | JACKET FRISCO               |
| ANGELA      | KWAI HOMEWARD               |
| ANGELA      | LUCKY FLYING                |
| ANGELA      | MOTHER OLEANDER             |
| ANGELA      | PEAK FOREVER                |
| ANGELA      | PULP BEVERLY                |
| ANGELA      | RUSH GOODFELLAS             |
| ANGELA      | SASSY PACKER                |
| ANGELA      | SECRET GROUNDHOG            |
| ANGELA      | SHAWSHANK BUBBLE            |
| ANGELA      | STEPMOM DREAM               |
| ANGELA      | TOMATOES HELLFIGHTERS       |
| ANGELA      | WAIT CIDER                  |
| KIM         | ARMAGEDDON LOST             |
| KIM         | BUTTERFLY CHOCOLAT          |
| KIM         | CARIBBEAN LIBERTY           |
| KIM         | CLASH FREDDY                |
| KIM         | CLEOPATRA DEVIL             |
| KIM         | DOORS PRESIDENT             |
| KIM         | EXORCIST STING              |
| KIM         | HARPER DYING                |
| KIM         | HEARTBREAKERS BRIGHT        |
| KIM         | INDEPENDENCE HOTEL          |
| KIM         | JAPANESE RUN                |
| KIM         | JINGLE SAGEBRUSH            |
| KIM         | KARATE MOON                 |
| KIM         | LOLA AGENT                  |
| KIM         | MONSTER SPARTACUS           |
| KIM         | NONE SPIKING                |
| KIM         | NOTORIOUS REUNION           |
| KIM         | ORANGE GRAPES               |
| KIM         | PAST SUICIDES               |
| KIM         | PATRIOT ROMAN               |
| KIM         | POTLUCK MIXED               |
| KIM         | RAINBOW SHOCK               |
| KIM         | RESERVOIR ADAPTATION        |
| KIM         | RUGRATS SHAKESPEARE         |
| KIM         | SOUP WISDOM                 |
| KIM         | TITANS JERK                 |
| KIM         | UNFAITHFUL KILL             |
| KIM         | WAIT CIDER                  |
| ALBERT      | ALASKA PHANTOM              |
| ALBERT      | ALLEY EVOLUTION             |
| ALBERT      | APOLLO TEEN                 |
| ALBERT      | CANDLES GRAPES              |
| ALBERT      | CONNECTICUT TRAMP           |
| ALBERT      | CROOKED FROGMEN             |
| ALBERT      | CRUSADE HONEY               |
| ALBERT      | DANGEROUS UPTOWN            |
| ALBERT      | DECEIVER BETRAYED           |
| ALBERT      | ELF MURDER                  |
| ALBERT      | EXPRESS LONELY              |
| ALBERT      | FIGHT JAWBREAKER            |
| ALBERT      | FLAMINGOS CONNECTICUT       |
| ALBERT      | GRACELAND DYNAMITE          |
| ALBERT      | GROSSE WONDERFUL            |
| ALBERT      | HARPER DYING                |
| ALBERT      | HEAVEN FREEDOM              |
| ALBERT      | HOMEWARD CIDER              |
| ALBERT      | HONEY TIES                  |
| ALBERT      | LEAGUE HELLFIGHTERS         |
| ALBERT      | LEBOWSKI SOLDIERS           |
| ALBERT      | METAL ARMAGEDDON            |
| ALBERT      | MONSOON CAUSE               |
| ALBERT      | REDEMPTION COMFORTS         |
| ALBERT      | RIGHT CRANES                |
| ALBERT      | ROAD ROXANNE                |
| ALBERT      | SWEDEN SHINING              |
| ALBERT      | TREASURE COMMAND            |
| ALBERT      | UNDEFEATED DALMATIONS       |
| ALBERT      | VIRGINIAN PLUTO             |
| ALBERT      | WALLS ARTIST                |
| ALBERT      | WEDDING APOLLO              |
| ALBERT      | WEST LION                   |
| FAY         | AFFAIR PREJUDICE            |
| FAY         | BONNIE HOLOCAUST            |
| FAY         | CENTER DINOSAUR             |
| FAY         | CHASING FIGHT               |
| FAY         | CHISUM BEHAVIOR             |
| FAY         | CONNECTION MICROCOSMOS      |
| FAY         | DRAGONFLY STRANGERS         |
| FAY         | DRIVER ANNIE                |
| FAY         | EXPENDABLE STALLION         |
| FAY         | EYES DRIVING                |
| FAY         | FATAL HAUNTED               |
| FAY         | FEVER EMPIRE                |
| FAY         | FIREHOUSE VIETNAM           |
| FAY         | FREAKY POCUS                |
| FAY         | FROST HEAD                  |
| FAY         | GASLIGHT CRUSADE            |
| FAY         | HAMLET WISDOM               |
| FAY         | HARPER DYING                |
| FAY         | HAUNTED ANTITRUST           |
| FAY         | HEAVEN FREEDOM              |
| FAY         | HOOSIERS BIRDCAGE           |
| FAY         | HURRICANE AFFAIR            |
| FAY         | LAMBS CINCINATTI            |
| FAY         | MALKOVICH PET               |
| FAY         | MASSACRE USUAL              |
| FAY         | OZ LIAISONS                 |
| FAY         | POLISH BROOKLYN             |
| FAY         | QUILLS BULL                 |
| FAY         | SUNDANCE INVASION           |
| FAY         | WAR NOTTING                 |
| FAY         | WORDS HUNTER                |
| EMILY       | ANONYMOUS HUMAN             |
| EMILY       | BASIC EASY                  |
| EMILY       | CHAMBER ITALIAN             |
| EMILY       | CHRISTMAS MOONSHINE         |
| EMILY       | DESTINY SATURDAY            |
| EMILY       | FUGITIVE MAGUIRE            |
| EMILY       | GONE TROUBLE                |
| EMILY       | HOLLOW JEOPARDY             |
| EMILY       | INVASION CYCLONE            |
| EMILY       | OCTOBER SUBMARINE           |
| EMILY       | REBEL AIRPORT               |
| EMILY       | SCARFACE BANG               |
| EMILY       | SEA VIRGIN                  |
| EMILY       | SHREK LICENSE               |
| RUSSELL     | BANG KWAI                   |
| RUSSELL     | BILL OTHERS                 |
| RUSSELL     | BREAKFAST GOLDFINGER        |
| RUSSELL     | CANYON STOCK                |
| RUSSELL     | CHASING FIGHT               |
| RUSSELL     | CHITTY LOCK                 |
| RUSSELL     | CITIZEN SHREK               |
| RUSSELL     | CLOSER BANG                 |
| RUSSELL     | COMFORTS RUSH               |
| RUSSELL     | CONNECTION MICROCOSMOS      |
| RUSSELL     | CRAZY HOME                  |
| RUSSELL     | CROSSROADS CASUALTIES       |
| RUSSELL     | FROGMEN BREAKING            |
| RUSSELL     | GHOST GROUNDHOG             |
| RUSSELL     | GLORY TRACY                 |
| RUSSELL     | GOLD RIVER                  |
| RUSSELL     | INDIAN LOVE                 |
| RUSSELL     | NOVOCAINE FLIGHT            |
| RUSSELL     | PELICAN COMFORTS            |
| RUSSELL     | PLATOON INSTINCT            |
| RUSSELL     | SANTA PARIS                 |
| RUSSELL     | SHAKESPEARE SADDLE          |
| RUSSELL     | SLUMS DUCK                  |
| RUSSELL     | SMILE EARRING               |
| RUSSELL     | TOWERS HURRICANE            |
| RUSSELL     | TRAINSPOTTING STRANGERS     |
| RUSSELL     | TROOPERS METAL              |
| RUSSELL     | UNCUT SUICIDES              |
| RUSSELL     | VISION TORQUE               |
| RUSSELL     | VOLCANO TEXAS               |
| RUSSELL     | WRATH MILE                  |
| JAYNE       | ANACONDA CONFESSIONS        |
| JAYNE       | BEDAZZLED MARRIED           |
| JAYNE       | BIRD INDEPENDENCE           |
| JAYNE       | BRAVEHEART HUMAN            |
| JAYNE       | BULL SHAWSHANK              |
| JAYNE       | COMANCHEROS ENEMY           |
| JAYNE       | CREEPERS KANE               |
| JAYNE       | DANCING FEVER               |
| JAYNE       | DISCIPLE MOTHER             |
| JAYNE       | EARTH VISION                |
| JAYNE       | ENGLISH BULWORTH            |
| JAYNE       | FEATHERS METAL              |
| JAYNE       | GUMP DATE                   |
| JAYNE       | HORN WORKING                |
| JAYNE       | HYSTERICAL GRAIL            |
| JAYNE       | ICE CROSSING                |
| JAYNE       | INVASION CYCLONE            |
| JAYNE       | LAMBS CINCINATTI            |
| JAYNE       | LUST LOCK                   |
| JAYNE       | MAIDEN HOME                 |
| JAYNE       | NOTORIOUS REUNION           |
| JAYNE       | OUTFIELD MASSACRE           |
| JAYNE       | PERFECT GROOVE              |
| JAYNE       | PRIMARY GLASS               |
| JAYNE       | REUNION WITCHES             |
| JAYNE       | SECRETARY ROUGE             |
| JAYNE       | STRANGERS GRAFFITI          |
| JAYNE       | SWEETHEARTS SUSPECTS        |
| JAYNE       | TELEMARK HEARTBREAKERS      |
| JAYNE       | THIEF PELICAN               |
| JAYNE       | TIES HUNGER                 |
| JAYNE       | TITANIC BOONDOCK            |
| JAYNE       | WAIT CIDER                  |
| JAYNE       | WASTELAND DIVINE            |
| GEOFFREY    | CENTER DINOSAUR             |
| GEOFFREY    | CHINATOWN GLADIATOR         |
| GEOFFREY    | COMA HEAD                   |
| GEOFFREY    | COMMAND DARLING             |
| GEOFFREY    | DAZED PUNK                  |
| GEOFFREY    | DIRTY ACE                   |
| GEOFFREY    | FUGITIVE MAGUIRE            |
| GEOFFREY    | GOLDMINE TYCOON             |
| GEOFFREY    | GORGEOUS BINGO              |
| GEOFFREY    | GRIT CLOCKWORK              |
| GEOFFREY    | IGBY MAKER                  |
| GEOFFREY    | INSTINCT AIRPORT            |
| GEOFFREY    | JEOPARDY ENCINO             |
| GEOFFREY    | KISSING DOLLS               |
| GEOFFREY    | LOLA AGENT                  |
| GEOFFREY    | LUCK OPUS                   |
| GEOFFREY    | MERMAID INSECTS             |
| GEOFFREY    | MIDNIGHT WESTWARD           |
| GEOFFREY    | ODDS BOOGIE                 |
| GEOFFREY    | PARIS WEEKEND               |
| GEOFFREY    | PATTON INTERVIEW            |
| GEOFFREY    | PUNK DIVORCE                |
| GEOFFREY    | TELEMARK HEARTBREAKERS      |
| GEOFFREY    | TITANIC BOONDOCK            |
| GEOFFREY    | TOMORROW HUSTLER            |
| GEOFFREY    | WORKING MICROCOSMOS         |
| BEN         | BEAR GRACELAND              |
| BEN         | CITIZEN SHREK               |
| BEN         | DAZED PUNK                  |
| BEN         | DOZEN LION                  |
| BEN         | FIREHOUSE VIETNAM           |
| BEN         | FRANKENSTEIN STRANGER       |
| BEN         | JAPANESE RUN                |
| BEN         | JASON TRAP                  |
| BEN         | MILLION ACE                 |
| BEN         | MUPPET MILE                 |
| BEN         | MUSKETEERS WAIT             |
| BEN         | NASH CHOCOLAT               |
| BEN         | PET HAUNTING                |
| BEN         | PINOCCHIO SIMON             |
| BEN         | RIDER CADDYSHACK            |
| BEN         | SCARFACE BANG               |
| BEN         | SORORITY QUEEN              |
| BEN         | STING PERSONAL              |
| BEN         | TIMBERLAND SKY              |
| BEN         | TOURIST PELICAN             |
| BEN         | UPRISING UPTOWN             |
| BEN         | WATERFRONT DELIVERANCE      |
| BEN         | WEREWOLF LOLA               |
| MINNIE      | BABY HALL                   |
| MINNIE      | BEETHOVEN EXORCIST          |
| MINNIE      | CHAPLIN LICENSE             |
| MINNIE      | CONSPIRACY SPIRIT           |
| MINNIE      | DAISY MENAGERIE             |
| MINNIE      | DINOSAUR SECRETARY          |
| MINNIE      | HUSTLER PARTY               |
| MINNIE      | JASON TRAP                  |
| MINNIE      | JEEPERS WEDDING             |
| MINNIE      | JET NEIGHBORS               |
| MINNIE      | LOVELY JINGLE               |
| MINNIE      | NORTH TEQUILA               |
| MINNIE      | RINGS HEARTBREAKERS         |
| MINNIE      | SADDLE ANTITRUST            |
| MINNIE      | SAVANNAH TOWN               |
| MINNIE      | SOLDIERS EVOLUTION          |
| MINNIE      | STOCK GLASS                 |
| MINNIE      | TYCOON GATHERING            |
| MINNIE      | VELVET TERMINATOR           |
| MINNIE      | WORKER TARZAN               |
| MERYL       | ANONYMOUS HUMAN             |
| MERYL       | CADDYSHACK JEDI             |
| MERYL       | CHICAGO NORTH               |
| MERYL       | CLONES PINOCCHIO            |
| MERYL       | COMFORTS RUSH               |
| MERYL       | COMMAND DARLING             |
| MERYL       | CROSSROADS CASUALTIES       |
| MERYL       | DARES PLUTO                 |
| MERYL       | EGG IGBY                    |
| MERYL       | ELEMENT FREDDY              |
| MERYL       | ENCOUNTERS CURTAIN          |
| MERYL       | FACTORY DRAGON              |
| MERYL       | FIGHT JAWBREAKER            |
| MERYL       | HANGING DEEP                |
| MERYL       | HAPPINESS UNITED            |
| MERYL       | HOLIDAY GAMES               |
| MERYL       | HUNGER ROOF                 |
| MERYL       | INTRIGUE WORST              |
| MERYL       | JADE BUNCH                  |
| MERYL       | JUGGLER HARDLY              |
| MERYL       | MODEL FISH                  |
| MERYL       | MOURNING PURPLE             |
| MERYL       | PINOCCHIO SIMON             |
| MERYL       | PRINCESS GIANT              |
| MERYL       | SKY MIRACLE                 |
| MERYL       | STATE WASTELAND             |
| MERYL       | WAKE JAWS                   |
| MERYL       | WORKER TARZAN               |
| IAN         | AMELIE HELLFIGHTERS         |
| IAN         | BERETS AGENT                |
| IAN         | CATCH AMISTAD               |
| IAN         | CITIZEN SHREK               |
| IAN         | DEER VIRGINIAN              |
| IAN         | DRACULA CRYSTAL             |
| IAN         | FANTASY TROOPERS            |
| IAN         | FIDDLER LOST                |
| IAN         | GLADIATOR WESTWARD          |
| IAN         | GLEAMING JAWBREAKER         |
| IAN         | GROOVE FICTION              |
| IAN         | GUN BONNIE                  |
| IAN         | HAWK CHILL                  |
| IAN         | HOMEWARD CIDER              |
| IAN         | INFORMER DOUBLE             |
| IAN         | LEATHERNECKS DWARFS         |
| IAN         | MIXED DOORS                 |
| IAN         | MONEY HAROLD                |
| IAN         | NOTTING SPEAKEASY           |
| IAN         | POLISH BROOKLYN             |
| IAN         | SAGEBRUSH CLUELESS          |
| IAN         | SCARFACE BANG               |
| IAN         | SHAWSHANK BUBBLE            |
| IAN         | STORM HAPPINESS             |
| IAN         | TEXAS WATCH                 |
| IAN         | TIGHTS DAWN                 |
| IAN         | VIDEOTAPE ARSENIC           |
| IAN         | WEDDING APOLLO              |
| IAN         | WORDS HUNTER                |
| IAN         | YOUTH KICK                  |
| IAN         | ZORRO ARK                   |
| FAY         | BANG KWAI                   |
| FAY         | CLEOPATRA DEVIL             |
| FAY         | CRYSTAL BREAKING            |
| FAY         | DORADO NOTTING              |
| FAY         | DUMBO LUST                  |
| FAY         | DURHAM PANKY                |
| FAY         | ENGLISH BULWORTH            |
| FAY         | EXTRAORDINARY CONQUERER     |
| FAY         | FAMILY SWEET                |
| FAY         | GANGS PRIDE                 |
| FAY         | GREEDY ROOTS                |
| FAY         | IDAHO LOVE                  |
| FAY         | INSIDER ARIZONA             |
| FAY         | INTRIGUE WORST              |
| FAY         | KWAI HOMEWARD               |
| FAY         | LIAISONS SWEET              |
| FAY         | MONTEREY LABYRINTH          |
| FAY         | OUTBREAK DIVINE             |
| FAY         | PURPLE MOVIE                |
| FAY         | RUSHMORE MERMAID            |
| FAY         | SEATTLE EXPECATIONS         |
| FAY         | STEERS ARMAGEDDON           |
| GRETA       | ALADDIN CALENDAR            |
| GRETA       | ANALYZE HOOSIERS            |
| GRETA       | ARABIA DOGMA                |
| GRETA       | CARRIE BUNCH                |
| GRETA       | CLOSER BANG                 |
| GRETA       | CONVERSATION DOWNHILL       |
| GRETA       | DARKO DORADO                |
| GRETA       | DAZED PUNK                  |
| GRETA       | EVOLUTION ALTER             |
| GRETA       | FANTASY TROOPERS            |
| GRETA       | FLASH WARS                  |
| GRETA       | FLYING HOOK                 |
| GRETA       | GENTLEMEN STAGE             |
| GRETA       | HARDLY ROBBERS              |
| GRETA       | HAUNTING PIANIST            |
| GRETA       | HOOSIERS BIRDCAGE           |
| GRETA       | KICK SAVANNAH               |
| GRETA       | LOVE SUICIDES               |
| GRETA       | MICROCOSMOS PARADISE        |
| GRETA       | MIDNIGHT WESTWARD           |
| GRETA       | MULAN MOON                  |
| GRETA       | NATIONAL STORY              |
| GRETA       | ORDER BETRAYED              |
| GRETA       | PAST SUICIDES               |
| GRETA       | PRIDE ALAMO                 |
| GRETA       | RAINBOW SHOCK               |
| GRETA       | SKY MIRACLE                 |
| GRETA       | SPY MILE                    |
| GRETA       | TADPOLE PARK                |
| GRETA       | TROOPERS METAL              |
| GRETA       | WEEKEND PERSONAL            |
| GRETA       | WIFE TURN                   |
| VIVIEN      | APOCALYPSE FLAMINGOS        |
| VIVIEN      | BABY HALL                   |
| VIVIEN      | BEETHOVEN EXORCIST          |
| VIVIEN      | BENEATH RUSH                |
| VIVIEN      | BUBBLE GROSSE               |
| VIVIEN      | CAROL TEXAS                 |
| VIVIEN      | CONNECTICUT TRAMP           |
| VIVIEN      | CONNECTION MICROCOSMOS      |
| VIVIEN      | CRAZY HOME                  |
| VIVIEN      | DAWN POND                   |
| VIVIEN      | DONNIE ALLEY                |
| VIVIEN      | EXORCIST STING              |
| VIVIEN      | HOUSE DYNAMITE              |
| VIVIEN      | JACKET FRISCO               |
| VIVIEN      | JERICHO MULAN               |
| VIVIEN      | LOSER HUSTLER               |
| VIVIEN      | MALLRATS UNITED             |
| VIVIEN      | MINORITY KISS               |
| VIVIEN      | MOULIN WAKE                 |
| VIVIEN      | NATIONAL STORY              |
| VIVIEN      | NOON PAPI                   |
| VIVIEN      | OPEN AFRICAN                |
| VIVIEN      | SIMON NORTH                 |
| VIVIEN      | SMOKING BARBARELLA          |
| VIVIEN      | SPARTACUS CHEAPER           |
| VIVIEN      | SPIRIT FLINTSTONES          |
| VIVIEN      | STAMPEDE DISTURBING         |
| VIVIEN      | SUSPECTS QUILLS             |
| VIVIEN      | TELEGRAPH VOYAGE            |
| VIVIEN      | TELEMARK HEARTBREAKERS      |
| VIVIEN      | TOMATOES HELLFIGHTERS       |
| VIVIEN      | TOOTSIE PILOT               |
| VIVIEN      | WEEKEND PERSONAL            |
| VIVIEN      | WEREWOLF LOLA               |
| VIVIEN      | WORLD LEATHERNECKS          |
| LAURA       | AMELIE HELLFIGHTERS         |
| LAURA       | BLOOD ARGONAUTS             |
| LAURA       | CAT CONEHEADS               |
| LAURA       | CRANES RESERVOIR            |
| LAURA       | DANCING FEVER               |
| LAURA       | DARES PLUTO                 |
| LAURA       | DESIRE ALIEN                |
| LAURA       | DOZEN LION                  |
| LAURA       | FUGITIVE MAGUIRE            |
| LAURA       | FULL FLATLINERS             |
| LAURA       | FURY MURDER                 |
| LAURA       | GODFATHER DIARY             |
| LAURA       | HOBBIT ALIEN                |
| LAURA       | MAGNOLIA FORRESTER          |
| LAURA       | MASK PEACH                  |
| LAURA       | MOTIONS DETAILS             |
| LAURA       | PET HAUNTING                |
| LAURA       | PINOCCHIO SIMON             |
| LAURA       | SHANGHAI TYCOON             |
| LAURA       | SHOCK CABIN                 |
| LAURA       | SINNERS ATLANTIS            |
| LAURA       | SKY MIRACLE                 |
| LAURA       | SOMETHING DUCK              |
| LAURA       | TARZAN VIDEOTAPE            |
| LAURA       | TRANSLATION SUMMER          |
| LAURA       | WISDOM WORKER               |
| CHRIS       | ACE GOLDFINGER              |
| CHRIS       | ALONE TRIP                  |
| CHRIS       | ATLANTIS CAUSE              |
| CHRIS       | DOOM DANCING                |
| CHRIS       | EAGLES PANKY                |
| CHRIS       | EGYPT TENENBAUMS            |
| CHRIS       | GONE TROUBLE                |
| CHRIS       | IMPOSSIBLE PREJUDICE        |
| CHRIS       | IRON MOON                   |
| CHRIS       | JERK PAYCHECK               |
| CHRIS       | MINDS TRUMAN                |
| CHRIS       | PARTY KNOCK                 |
| CHRIS       | SABRINA MIDNIGHT            |
| CHRIS       | SCALAWAG DUCK               |
| CHRIS       | SCHOOL JACKET               |
| CHRIS       | SIDE ARK                    |
| CHRIS       | SPEED SUIT                  |
| CHRIS       | TEQUILA PAST                |
| CHRIS       | VOLUME HOUSE                |
| CHRIS       | WAKE JAWS                   |
| HARVEY      | ATLANTIS CAUSE              |
| HARVEY      | BEACH HEARTBREAKERS         |
| HARVEY      | BORROWERS BEDAZZLED         |
| HARVEY      | BOULEVARD MOB               |
| HARVEY      | CARIBBEAN LIBERTY           |
| HARVEY      | CRAZY HOME                  |
| HARVEY      | DOWNHILL ENOUGH             |
| HARVEY      | EARRING INSTINCT            |
| HARVEY      | ENCINO ELF                  |
| HARVEY      | FRONTIER CABIN              |
| HARVEY      | GENTLEMEN STAGE             |
| HARVEY      | HAROLD FRENCH               |
| HARVEY      | HELLFIGHTERS SIERRA         |
| HARVEY      | HOLY TADPOLE                |
| HARVEY      | IRON MOON                   |
| HARVEY      | LOCK REAR                   |
| HARVEY      | MODEL FISH                  |
| HARVEY      | OSCAR GOLD                  |
| HARVEY      | PANIC CLUB                  |
| HARVEY      | PANTHER REDS                |
| HARVEY      | PEARL DESTINY               |
| HARVEY      | PIZZA JUMANJI               |
| HARVEY      | RANDOM GO                   |
| HARVEY      | RULES HUMAN                 |
| HARVEY      | SLEUTH ORIENT               |
| HARVEY      | SPEAKEASY DATE              |
| HARVEY      | STORY SIDE                  |
| HARVEY      | TELEMARK HEARTBREAKERS      |
| HARVEY      | UNBREAKABLE KARATE          |
| HARVEY      | UNCUT SUICIDES              |
| HARVEY      | UNFORGIVEN ZOOLANDER        |
| HARVEY      | UPRISING UPTOWN             |
| OPRAH       | ACADEMY DINOSAUR            |
| OPRAH       | AFFAIR PREJUDICE            |
| OPRAH       | AIRPLANE SIERRA             |
| OPRAH       | ALTER VICTORY               |
| OPRAH       | ANTHEM LUKE                 |
| OPRAH       | APOCALYPSE FLAMINGOS        |
| OPRAH       | APOLLO TEEN                 |
| OPRAH       | ARSENIC INDEPENDENCE        |
| OPRAH       | BONNIE HOLOCAUST            |
| OPRAH       | CAROL TEXAS                 |
| OPRAH       | COAST RAINBOW               |
| OPRAH       | EGG IGBY                    |
| OPRAH       | ELIZABETH SHANE             |
| OPRAH       | HEARTBREAKERS BRIGHT        |
| OPRAH       | HEAVEN FREEDOM              |
| OPRAH       | HIGH ENCINO                 |
| OPRAH       | KISS GLORY                  |
| OPRAH       | MIDNIGHT WESTWARD           |
| OPRAH       | MUSSOLINI SPOILERS          |
| OPRAH       | OLEANDER CLUE               |
| OPRAH       | PARK CITIZEN                |
| OPRAH       | SHEPHERD MIDSUMMER          |
| OPRAH       | STEERS ARMAGEDDON           |
| OPRAH       | TREASURE COMMAND            |
| OPRAH       | WEREWOLF LOLA               |
| CHRISTOPHER | ANYTHING SAVANNAH           |
| CHRISTOPHER | ATTRACTION NEWTON           |
| CHRISTOPHER | COLOR PHILADELPHIA          |
| CHRISTOPHER | CONSPIRACY SPIRIT           |
| CHRISTOPHER | DOGMA FAMILY                |
| CHRISTOPHER | ENDING CROWDS               |
| CHRISTOPHER | FANTASY TROOPERS            |
| CHRISTOPHER | FARGO GANDHI                |
| CHRISTOPHER | FELLOWSHIP AUTUMN           |
| CHRISTOPHER | HAMLET WISDOM               |
| CHRISTOPHER | HEARTBREAKERS BRIGHT        |
| CHRISTOPHER | HORROR REIGN                |
| CHRISTOPHER | HUSTLER PARTY               |
| CHRISTOPHER | LIFE TWISTED                |
| CHRISTOPHER | RECORDS ZORRO               |
| CHRISTOPHER | SHAWSHANK BUBBLE            |
| CHRISTOPHER | SPLENDOR PATTON             |
| CHRISTOPHER | TEMPLE ATTRACTION           |
| CHRISTOPHER | TIMBERLAND SKY              |
| CHRISTOPHER | VISION TORQUE               |
| CHRISTOPHER | YOUNG LANGUAGE              |
| HUMPHREY    | ALIEN CENTER                |
| HUMPHREY    | ANACONDA CONFESSIONS        |
| HUMPHREY    | CHOCOLATE DUCK              |
| HUMPHREY    | COMFORTS RUSH               |
| HUMPHREY    | DREAM PICKUP                |
| HUMPHREY    | FLINTSTONES HAPPINESS       |
| HUMPHREY    | GAMES BOWFINGER             |
| HUMPHREY    | GOLDMINE TYCOON             |
| HUMPHREY    | HOOSIERS BIRDCAGE           |
| HUMPHREY    | IDAHO LOVE                  |
| HUMPHREY    | IRON MOON                   |
| HUMPHREY    | MADNESS ATTACKS             |
| HUMPHREY    | MUSIC BOONDOCK              |
| HUMPHREY    | MYSTIC TRUMAN               |
| HUMPHREY    | PERSONAL LADYBUGS           |
| HUMPHREY    | PIRATES ROXANNE             |
| HUMPHREY    | PRINCESS GIANT              |
| HUMPHREY    | SISTER FREDDY               |
| HUMPHREY    | SONS INTERVIEW              |
| HUMPHREY    | SPLASH GUMP                 |
| HUMPHREY    | SPOILERS HELLFIGHTERS       |
| HUMPHREY    | STRAIGHT HOURS              |
| HUMPHREY    | TERMINATOR CLUB             |
| HUMPHREY    | TRAP GUYS                   |
| HUMPHREY    | WAR NOTTING                 |
| HUMPHREY    | WONDERFUL DROP              |
| AL          | BILL OTHERS                 |
| AL          | BREAKFAST GOLDFINGER        |
| AL          | CHITTY LOCK                 |
| AL          | DALMATIONS SWEDEN           |
| AL          | DRIFTER COMMANDMENTS        |
| AL          | ENOUGH RAGING               |
| AL          | GLASS DYING                 |
| AL          | GRAIL FRANKENSTEIN          |
| AL          | HANDICAP BOONDOCK           |
| AL          | HOLIDAY GAMES               |
| AL          | HOUSE DYNAMITE              |
| AL          | JACKET FRISCO               |
| AL          | MUPPET MILE                 |
| AL          | OSCAR GOLD                  |
| AL          | PARK CITIZEN                |
| AL          | POTTER CONNECTICUT          |
| AL          | ROCK INSTINCT               |
| AL          | SENSE GREEK                 |
| AL          | SILVERADO GOLDFINGER        |
| AL          | SLEUTH ORIENT               |
| AL          | SLIPPER FIDELITY            |
| AL          | SPLASH GUMP                 |
| AL          | SPLENDOR PATTON             |
| AL          | VISION TORQUE               |
| AL          | VOICE PEACH                 |
| AL          | WASTELAND DIVINE            |
| NICK        | ANGELS LIFE                 |
| NICK        | ARK RIDGEMONT               |
| NICK        | BARBARELLA STREETCAR        |
| NICK        | BEAUTY GREASE               |
| NICK        | BETRAYED REAR               |
| NICK        | BOOGIE AMELIE               |
| NICK        | CHITTY LOCK                 |
| NICK        | DRIVING POLISH              |
| NICK        | EXTRAORDINARY CONQUERER     |
| NICK        | FEATHERS METAL              |
| NICK        | FLYING HOOK                 |
| NICK        | GLEAMING JAWBREAKER         |
| NICK        | GOLDFINGER SENSIBILITY      |
| NICK        | HOME PITY                   |
| NICK        | MINE TITANS                 |
| NICK        | NEWSIES STORY               |
| NICK        | PET HAUNTING                |
| NICK        | RANDOM GO                   |
| NICK        | SHIP WONDERLAND             |
| NICK        | SUPER WYOMING               |
| NICK        | VIRGIN DAISY                |
| NICK        | ZORRO ARK                   |
| LAURENCE    | ALONE TRIP                  |
| LAURENCE    | ANGELS LIFE                 |
| LAURENCE    | BEDAZZLED MARRIED           |
| LAURENCE    | BILL OTHERS                 |
| LAURENCE    | BUNCH MINDS                 |
| LAURENCE    | CARIBBEAN LIBERTY           |
| LAURENCE    | CROOKED FROGMEN             |
| LAURENCE    | EXPECATIONS NATURAL         |
| LAURENCE    | FISH OPUS                   |
| LAURENCE    | FROGMEN BREAKING            |
| LAURENCE    | FROST HEAD                  |
| LAURENCE    | KICK SAVANNAH               |
| LAURENCE    | MALKOVICH PET               |
| LAURENCE    | NOON PAPI                   |
| LAURENCE    | NORTHWEST POLISH            |
| LAURENCE    | PERFECT GROOVE              |
| LAURENCE    | POTLUCK MIXED               |
| LAURENCE    | REAR TRADING                |
| LAURENCE    | ROAD ROXANNE                |
| LAURENCE    | SIDE ARK                    |
| LAURENCE    | SINNERS ATLANTIS            |
| LAURENCE    | SKY MIRACLE                 |
| LAURENCE    | STREETCAR INTENTIONS        |
| LAURENCE    | SUNDANCE INVASION           |
| LAURENCE    | TENENBAUMS COMMAND          |
| LAURENCE    | UNFAITHFUL KILL             |
| WILL        | APOCALYPSE FLAMINGOS        |
| WILL        | BAREFOOT MANCHURIAN         |
| WILL        | BOWFINGER GABLES            |
| WILL        | CAMPUS REMEMBER             |
| WILL        | CRAZY HOME                  |
| WILL        | CRUELTY UNFORGIVEN          |
| WILL        | DARES PLUTO                 |
| WILL        | DIVORCE SHINING             |
| WILL        | DONNIE ALLEY                |
| WILL        | DRIVING POLISH              |
| WILL        | FATAL HAUNTED               |
| WILL        | FRENCH HOLIDAY              |
| WILL        | GUN BONNIE                  |
| WILL        | HORN WORKING                |
| WILL        | HUMAN GRAFFITI              |
| WILL        | LIBERTY MAGNIFICENT         |
| WILL        | MOURNING PURPLE             |
| WILL        | NEIGHBORS CHARADE           |
| WILL        | NOON PAPI                   |
| WILL        | PAJAMA JAWBREAKER           |
| WILL        | PICKUP DRIVING              |
| WILL        | PLATOON INSTINCT            |
| WILL        | SLEEPING SUSPECTS           |
| WILL        | SLEUTH ORIENT               |
| WILL        | SPEED SUIT                  |
| WILL        | STAR OPERATION              |
| WILL        | THEORY MERMAID              |
| WILL        | TIES HUNGER                 |
| WILL        | TITANIC BOONDOCK            |
| WILL        | UPRISING UPTOWN             |
| WILL        | WARLOCK WEREWOLF            |
| KENNETH     | AGENT TRUMAN                |
| KENNETH     | BLACKOUT PRIVATE            |
| KENNETH     | BRANNIGAN SUNRISE           |
| KENNETH     | DOUBTFIRE LABYRINTH         |
| KENNETH     | DOZEN LION                  |
| KENNETH     | EVE RESURRECTION            |
| KENNETH     | FAMILY SWEET                |
| KENNETH     | FLYING HOOK                 |
| KENNETH     | GANGS PRIDE                 |
| KENNETH     | GRACELAND DYNAMITE          |
| KENNETH     | HANOVER GALAXY              |
| KENNETH     | HORROR REIGN                |
| KENNETH     | LABYRINTH LEAGUE            |
| KENNETH     | MASSAGE IMAGE               |
| KENNETH     | METAL ARMAGEDDON            |
| KENNETH     | ODDS BOOGIE                 |
| KENNETH     | ORDER BETRAYED              |
| KENNETH     | PERSONAL LADYBUGS           |
| KENNETH     | PREJUDICE OLEANDER          |
| KENNETH     | RESURRECTION SILVERADO      |
| KENNETH     | SECRETS PARADISE            |
| KENNETH     | SNATCHERS MONTEZUMA         |
| KENNETH     | STOCK GLASS                 |
| KENNETH     | STORM HAPPINESS             |
| KENNETH     | TOMATOES HELLFIGHTERS       |
| KENNETH     | TORQUE BOUND                |
| KENNETH     | WAKE JAWS                   |
| KENNETH     | WRATH MILE                  |
| KENNETH     | ZHIVAGO CORE                |
| MENA        | AIRPLANE SIERRA             |
| MENA        | ALIEN CENTER                |
| MENA        | ANONYMOUS HUMAN             |
| MENA        | APOLLO TEEN                 |
| MENA        | BUBBLE GROSSE               |
| MENA        | CHASING FIGHT               |
| MENA        | CONSPIRACY SPIRIT           |
| MENA        | CORE SUIT                   |
| MENA        | DARN FORRESTER              |
| MENA        | FACTORY DRAGON              |
| MENA        | FLATLINERS KILLER           |
| MENA        | GILMORE BOILED              |
| MENA        | HIGHBALL POTTER             |
| MENA        | LAMBS CINCINATTI            |
| MENA        | LOVER TRUMAN                |
| MENA        | PURPLE MOVIE                |
| MENA        | SAINTS BRIDE                |
| MENA        | SATURDAY LAMBS              |
| MENA        | SUPERFLY TRIP               |
| MENA        | TAXI KICK                   |
| MENA        | THEORY MERMAID              |
| MENA        | UNITED PILOT                |
| MENA        | WRONG BEHAVIOR              |
| MENA        | YOUNG LANGUAGE              |
| OLYMPIA     | BADMAN DAWN                 |
| OLYMPIA     | CHITTY LOCK                 |
| OLYMPIA     | COLOR PHILADELPHIA          |
| OLYMPIA     | CONTACT ANONYMOUS           |
| OLYMPIA     | DEEP CRUSADE                |
| OLYMPIA     | EFFECT GLADIATOR            |
| OLYMPIA     | EXPRESS LONELY              |
| OLYMPIA     | FIREHOUSE VIETNAM           |
| OLYMPIA     | FUGITIVE MAGUIRE            |
| OLYMPIA     | HANKY OCTOBER               |
| OLYMPIA     | ICE CROSSING                |
| OLYMPIA     | IDOLS SNATCHERS             |
| OLYMPIA     | INTOLERABLE INTENTIONS      |
| OLYMPIA     | MAGNOLIA FORRESTER          |
| OLYMPIA     | MARS ROMAN                  |
| OLYMPIA     | MAUDE MOD                   |
| OLYMPIA     | MURDER ANTITRUST            |
| OLYMPIA     | NONE SPIKING                |
| OLYMPIA     | OTHERS SOUP                 |
| OLYMPIA     | PSYCHO SHRUNK               |
| OLYMPIA     | SANTA PARIS                 |
| OLYMPIA     | SENSE GREEK                 |
| OLYMPIA     | STORM HAPPINESS             |
| OLYMPIA     | SWEET BROTHERHOOD           |
| OLYMPIA     | TITANIC BOONDOCK            |
| OLYMPIA     | TOURIST PELICAN             |
| OLYMPIA     | TRAFFIC HOBBIT              |
| OLYMPIA     | WAIT CIDER                  |
| GROUCHO     | BASIC EASY                  |
| GROUCHO     | BROOKLYN DESERT             |
| GROUCHO     | CHOCOLATE DUCK              |
| GROUCHO     | DAWN POND                   |
| GROUCHO     | FANTASIA PARK               |
| GROUCHO     | GABLES METROPOLIS           |
| GROUCHO     | GONE TROUBLE                |
| GROUCHO     | GROUNDHOG UNCUT             |
| GROUCHO     | HOLLYWOOD ANONYMOUS         |
| GROUCHO     | JINGLE SAGEBRUSH            |
| GROUCHO     | KANE EXORCIST               |
| GROUCHO     | LONELY ELEPHANT             |
| GROUCHO     | LOVERBOY ATTACKS            |
| GROUCHO     | MEET CHOCOLATE              |
| GROUCHO     | MUSCLE BRIGHT               |
| GROUCHO     | OPPOSITE NECKLACE           |
| GROUCHO     | OZ LIAISONS                 |
| GROUCHO     | PAST SUICIDES               |
| GROUCHO     | PEACH INNOCENT              |
| GROUCHO     | RAGE GAMES                  |
| GROUCHO     | ROOTS REMEMBER              |
| GROUCHO     | SAINTS BRIDE                |
| GROUCHO     | SCORPION APOLLO             |
| GROUCHO     | SPLENDOR PATTON             |
| GROUCHO     | WARLOCK WEREWOLF            |
| ALAN        | BADMAN DAWN                 |
| ALAN        | BARBARELLA STREETCAR        |
| ALAN        | BIRCH ANTITRUST             |
| ALAN        | BLANKET BEVERLY             |
| ALAN        | BULWORTH COMMANDMENTS       |
| ALAN        | CLASH FREDDY                |
| ALAN        | CLUELESS BUCKET             |
| ALAN        | CRAZY HOME                  |
| ALAN        | DIVIDE MONSTER              |
| ALAN        | FIDELITY DEVIL              |
| ALAN        | GREEDY ROOTS                |
| ALAN        | HAUNTED ANTITRUST           |
| ALAN        | JUMPING WRATH               |
| ALAN        | KICK SAVANNAH               |
| ALAN        | LONELY ELEPHANT             |
| ALAN        | MAGUIRE APACHE              |
| ALAN        | MASSAGE IMAGE               |
| ALAN        | METAL ARMAGEDDON            |
| ALAN        | MONSTER SPARTACUS           |
| ALAN        | POLISH BROOKLYN             |
| ALAN        | RUSH GOODFELLAS             |
| ALAN        | SAGEBRUSH CLUELESS          |
| ALAN        | STRANGELOVE DESIRE          |
| ALAN        | STRICTLY SCARFACE           |
| ALAN        | UNCUT SUICIDES              |
| ALAN        | UPTOWN YOUNG                |
| ALAN        | VAMPIRE WHALE               |
| MICHAEL     | ALAMO VIDEOTAPE             |
| MICHAEL     | BEAUTY GREASE               |
| MICHAEL     | COMANCHEROS ENEMY           |
| MICHAEL     | EYES DRIVING                |
| MICHAEL     | GATHERING CALENDAR          |
| MICHAEL     | HUNTING MUSKETEERS          |
| MICHAEL     | IGBY MAKER                  |
| MICHAEL     | KICK SAVANNAH               |
| MICHAEL     | MUSIC BOONDOCK              |
| MICHAEL     | NECKLACE OUTBREAK           |
| MICHAEL     | NEWSIES STORY               |
| MICHAEL     | PARK CITIZEN                |
| MICHAEL     | PIANIST OUTFIELD            |
| MICHAEL     | PURPLE MOVIE                |
| MICHAEL     | REEF SALUTE                 |
| MICHAEL     | SENSIBILITY REAR            |
| MICHAEL     | SILENCE KANE                |
| MICHAEL     | SLIPPER FIDELITY            |
| MICHAEL     | SPICE SORORITY              |
| MICHAEL     | SPIRIT FLINTSTONES          |
| MICHAEL     | STRANGELOVE DESIRE          |
| MICHAEL     | STRANGER STRANGERS          |
| MICHAEL     | TELEGRAPH VOYAGE            |
| MICHAEL     | WOMEN DORADO                |
| WILLIAM     | ALABAMA DEVIL               |
| WILLIAM     | ANTITRUST TOMATOES          |
| WILLIAM     | BERETS AGENT                |
| WILLIAM     | CAUSE DATE                  |
| WILLIAM     | CLEOPATRA DEVIL             |
| WILLIAM     | CREEPERS KANE               |
| WILLIAM     | CROOKED FROGMEN             |
| WILLIAM     | GLORY TRACY                 |
| WILLIAM     | HAUNTED ANTITRUST           |
| WILLIAM     | HOLOCAUST HIGHBALL          |
| WILLIAM     | HUNCHBACK IMPOSSIBLE        |
| WILLIAM     | HUNTING MUSKETEERS          |
| WILLIAM     | JERICHO MULAN               |
| WILLIAM     | MONSOON CAUSE               |
| WILLIAM     | MOONSHINE CABIN             |
| WILLIAM     | NATIONAL STORY              |
| WILLIAM     | RECORDS ZORRO               |
| WILLIAM     | RIDER CADDYSHACK            |
| WILLIAM     | SEA VIRGIN                  |
| WILLIAM     | SECRETS PARADISE            |
| WILLIAM     | SPIKING ELEMENT             |
| WILLIAM     | STATE WASTELAND             |
| WILLIAM     | TIGHTS DAWN                 |
| WILLIAM     | TRAP GUYS                   |
| WILLIAM     | WINDOW SIDE                 |
| WILLIAM     | WISDOM WORKER               |
| WILLIAM     | ZHIVAGO CORE                |
| JON         | ALI FOREVER                 |
| JON         | BINGO TALENTED              |
| JON         | BORROWERS BEDAZZLED         |
| JON         | CIDER DESIRE                |
| JON         | CLUELESS BUCKET             |
| JON         | DOCTOR GRAIL                |
| JON         | DREAM PICKUP                |
| JON         | FANTASY TROOPERS            |
| JON         | FLAMINGOS CONNECTICUT       |
| JON         | HAROLD FRENCH               |
| JON         | HILLS NEIGHBORS             |
| JON         | HUNTER ALTER                |
| JON         | INDIAN LOVE                 |
| JON         | INSECTS STONE               |
| JON         | LESSON CLEOPATRA            |
| JON         | LIES TREATMENT              |
| JON         | MADIGAN DORADO              |
| JON         | MICROCOSMOS PARADISE        |
| JON         | PRIVATE DROP                |
| JON         | RESERVOIR ADAPTATION        |
| JON         | ROLLERCOASTER BRINGING      |
| JON         | ROUGE SQUAD                 |
| JON         | SAINTS BRIDE                |
| JON         | SKY MIRACLE                 |
| JON         | SPICE SORORITY              |
| JON         | STALLION SUNDANCE           |
| JON         | SUGAR WONKA                 |
| JON         | SWEET BROTHERHOOD           |
| JON         | VIRTUAL SPOILERS            |
| GENE        | ALASKA PHANTOM              |
| GENE        | ARMAGEDDON LOST             |
| GENE        | BALLROOM MOCKINGBIRD        |
| GENE        | BARBARELLA STREETCAR        |
| GENE        | BOOGIE AMELIE               |
| GENE        | CONFUSED CANDLES            |
| GENE        | CRAZY HOME                  |
| GENE        | DIVIDE MONSTER              |
| GENE        | DIVORCE SHINING             |
| GENE        | EVE RESURRECTION            |
| GENE        | GO PURPLE                   |
| GENE        | HAROLD FRENCH               |
| GENE        | HORN WORKING                |
| GENE        | INDIAN LOVE                 |
| GENE        | LIFE TWISTED                |
| GENE        | MADIGAN DORADO              |
| GENE        | MASSACRE USUAL              |
| GENE        | OZ LIAISONS                 |
| GENE        | PITY BOUND                  |
| GENE        | PIZZA JUMANJI               |
| GENE        | RESERVOIR ADAPTATION        |
| GENE        | RUNAWAY TENENBAUMS          |
| GENE        | SATISFACTION CONFIDENTIAL   |
| GENE        | SATURDAY LAMBS              |
| GENE        | SPICE SORORITY              |
| GENE        | TREATMENT JEKYLL            |
| GENE        | WANDA CHAMBER               |
| LISA        | ANYTHING SAVANNAH           |
| LISA        | ARABIA DOGMA                |
| LISA        | BUTTERFLY CHOCOLAT          |
| LISA        | CHITTY LOCK                 |
| LISA        | CLUB GRAFFITI               |
| LISA        | COAST RAINBOW               |
| LISA        | CROW GREASE                 |
| LISA        | CRUSADE HONEY               |
| LISA        | EFFECT GLADIATOR            |
| LISA        | FICTION CHRISTMAS           |
| LISA        | HANKY OCTOBER               |
| LISA        | JERICHO MULAN               |
| LISA        | LESSON CLEOPATRA            |
| LISA        | LOVER TRUMAN                |
| LISA        | MOD SECRETARY               |
| LISA        | QUILLS BULL                 |
| LISA        | RIVER OUTLAW                |
| LISA        | ROOTS REMEMBER              |
| LISA        | SASSY PACKER                |
| LISA        | VACATION BOONDOCK           |
| LISA        | WILD APOLLO                 |
| LISA        | WON DARES                   |
| LISA        | ZORRO ARK                   |
| ED          | ANALYZE HOOSIERS            |
| ED          | ANONYMOUS HUMAN             |
| ED          | BEHAVIOR RUNAWAY            |
| ED          | BONNIE HOLOCAUST            |
| ED          | BUTTERFLY CHOCOLAT          |
| ED          | CENTER DINOSAUR             |
| ED          | CLOSER BANG                 |
| ED          | CROSSROADS CASUALTIES       |
| ED          | DRAGON SQUAD                |
| ED          | EVOLUTION ALTER             |
| ED          | GENTLEMEN STAGE             |
| ED          | HIGH ENCINO                 |
| ED          | INSTINCT AIRPORT            |
| ED          | INVASION CYCLONE            |
| ED          | JUGGLER HARDLY              |
| ED          | MAUDE MOD                   |
| ED          | MODEL FISH                  |
| ED          | PACIFIC AMISTAD             |
| ED          | PRINCESS GIANT              |
| ED          | RINGS HEARTBREAKERS         |
| ED          | ROCK INSTINCT               |
| ED          | SCHOOL JACKET               |
| ED          | SMILE EARRING               |
| ED          | SOLDIERS EVOLUTION          |
| ED          | STRANGELOVE DESIRE          |
| ED          | UNFORGIVEN ZOOLANDER        |
| ED          | VALENTINE VANISHING         |
| ED          | WARS PLUTO                  |
| ED          | WIND PHANTOM                |
| JEFF        | ALASKA PHANTOM              |
| JEFF        | APOLLO TEEN                 |
| JEFF        | CHINATOWN GLADIATOR         |
| JEFF        | CROWDS TELEMARK             |
| JEFF        | DRUMS DYNAMITE              |
| JEFF        | HUNTER ALTER                |
| JEFF        | LADY STAGE                  |
| JEFF        | MASK PEACH                  |
| JEFF        | MUSCLE BRIGHT               |
| JEFF        | NEWSIES STORY               |
| JEFF        | NORTHWEST POLISH            |
| JEFF        | PARADISE SABRINA            |
| JEFF        | REMEMBER DIARY              |
| JEFF        | RIDER CADDYSHACK            |
| JEFF        | RINGS HEARTBREAKERS         |
| JEFF        | SECRETARY ROUGE             |
| JEFF        | SLIPPER FIDELITY            |
| JEFF        | SMILE EARRING               |
| JEFF        | SONS INTERVIEW              |
| JEFF        | SPARTACUS CHEAPER           |
| JEFF        | STOCK GLASS                 |
| JEFF        | SUSPECTS QUILLS             |
| JEFF        | TADPOLE PARK                |
| JEFF        | WALLS ARTIST                |
| JEFF        | WATCH TRACY                 |
| MATTHEW     | AFRICAN EGG                 |
| MATTHEW     | ARMY FLINTSTONES            |
| MATTHEW     | BIRCH ANTITRUST             |
| MATTHEW     | BLACKOUT PRIVATE            |
| MATTHEW     | BLUES INSTINCT              |
| MATTHEW     | CIRCUS YOUTH                |
| MATTHEW     | CROWDS TELEMARK             |
| MATTHEW     | DISCIPLE MOTHER             |
| MATTHEW     | ENOUGH RAGING               |
| MATTHEW     | FAMILY SWEET                |
| MATTHEW     | FICTION CHRISTMAS           |
| MATTHEW     | GRINCH MASSAGE              |
| MATTHEW     | GUN BONNIE                  |
| MATTHEW     | HARRY IDAHO                 |
| MATTHEW     | HEARTBREAKERS BRIGHT        |
| MATTHEW     | HOLES BRANNIGAN             |
| MATTHEW     | HOUSE DYNAMITE              |
| MATTHEW     | INCH JET                    |
| MATTHEW     | LADYBUGS ARMAGEDDON         |
| MATTHEW     | LIFE TWISTED                |
| MATTHEW     | LUCK OPUS                   |
| MATTHEW     | LUST LOCK                   |
| MATTHEW     | MADRE GABLES                |
| MATTHEW     | MINDS TRUMAN                |
| MATTHEW     | MOONSHINE CABIN             |
| MATTHEW     | MULAN MOON                  |
| MATTHEW     | MUSCLE BRIGHT               |
| MATTHEW     | NONE SPIKING                |
| MATTHEW     | ROOTS REMEMBER              |
| MATTHEW     | SNOWMAN ROLLERCOASTER       |
| MATTHEW     | SQUAD FISH                  |
| MATTHEW     | SUPERFLY TRIP               |
| MATTHEW     | SWARM GOLD                  |
| MATTHEW     | TADPOLE PARK                |
| MATTHEW     | TITANIC BOONDOCK            |
| MATTHEW     | TRANSLATION SUMMER          |
| MATTHEW     | TRIP NEWTON                 |
| MATTHEW     | UNCUT SUICIDES              |
| MATTHEW     | WORST BANGER                |
| DEBBIE      | APOLLO TEEN                 |
| DEBBIE      | CLUB GRAFFITI               |
| DEBBIE      | FAMILY SWEET                |
| DEBBIE      | FLINTSTONES HAPPINESS       |
| DEBBIE      | GALAXY SWEETHEARTS          |
| DEBBIE      | GLORY TRACY                 |
| DEBBIE      | HALF OUTFIELD               |
| DEBBIE      | HEDWIG ALTER                |
| DEBBIE      | HOLIDAY GAMES               |
| DEBBIE      | HOUSE DYNAMITE              |
| DEBBIE      | MONEY HAROLD                |
| DEBBIE      | OPPOSITE NECKLACE           |
| DEBBIE      | PEAK FOREVER                |
| DEBBIE      | PIANIST OUTFIELD            |
| DEBBIE      | PILOT HOOSIERS              |
| DEBBIE      | PRESIDENT BANG              |
| DEBBIE      | RANDOM GO                   |
| DEBBIE      | REDEMPTION COMFORTS         |
| DEBBIE      | SONG HEDWIG                 |
| DEBBIE      | SPIKING ELEMENT             |
| DEBBIE      | STEPMOM DREAM               |
| DEBBIE      | SUNDANCE INVASION           |
| DEBBIE      | VICTORY ACADEMY             |
| DEBBIE      | WORLD LEATHERNECKS          |
| RUSSELL     | APOCALYPSE FLAMINGOS        |
| RUSSELL     | ARMY FLINTSTONES            |
| RUSSELL     | BILKO ANONYMOUS             |
| RUSSELL     | CALIFORNIA BIRDS            |
| RUSSELL     | FIDELITY DEVIL              |
| RUSSELL     | GUNFIGHT MOON               |
| RUSSELL     | GUNFIGHTER MUSSOLINI        |
| RUSSELL     | GUYS FALCON                 |
| RUSSELL     | KENTUCKIAN GIANT            |
| RUSSELL     | LICENSE WEEKEND             |
| RUSSELL     | MIGHTY LUCK                 |
| RUSSELL     | OLEANDER CLUE               |
| RUSSELL     | RANGE MOONWALKER            |
| RUSSELL     | STORY SIDE                  |
| RUSSELL     | SUMMER SCARFACE             |
| RUSSELL     | TROUBLE DATE                |
| RUSSELL     | VIDEOTAPE ARSENIC           |
| RUSSELL     | VOLCANO TEXAS               |
| RUSSELL     | WON DARES                   |
| HUMPHREY    | ARACHNOPHOBIA ROLLERCOASTER |
| HUMPHREY    | BOONDOCK BALLROOM           |
| HUMPHREY    | CHITTY LOCK                 |
| HUMPHREY    | COMFORTS RUSH               |
| HUMPHREY    | DELIVERANCE MULHOLLAND      |
| HUMPHREY    | FRENCH HOLIDAY              |
| HUMPHREY    | GOSFORD DONNIE              |
| HUMPHREY    | ILLUSION AMELIE             |
| HUMPHREY    | JET NEIGHBORS               |
| HUMPHREY    | JUNGLE CLOSER               |
| HUMPHREY    | KISS GLORY                  |
| HUMPHREY    | MIDNIGHT WESTWARD           |
| HUMPHREY    | MINE TITANS                 |
| HUMPHREY    | MOONWALKER FOOL             |
| HUMPHREY    | NASH CHOCOLAT               |
| HUMPHREY    | OPUS ICE                    |
| HUMPHREY    | ORDER BETRAYED              |
| HUMPHREY    | PACIFIC AMISTAD             |
| HUMPHREY    | PAST SUICIDES               |
| HUMPHREY    | PIZZA JUMANJI               |
| HUMPHREY    | ROSES TREASURE              |
| HUMPHREY    | SEA VIRGIN                  |
| HUMPHREY    | SHINING ROSES               |
| HUMPHREY    | SUPER WYOMING               |
| HUMPHREY    | WARLOCK WEREWOLF            |
| HUMPHREY    | WEDDING APOLLO              |
| HUMPHREY    | WEEKEND PERSONAL            |
| HUMPHREY    | WEST LION                   |
| HUMPHREY    | WONDERLAND CHRISTMAS        |
| MICHAEL     | AIRPLANE SIERRA             |
| MICHAEL     | BREAKFAST GOLDFINGER        |
| MICHAEL     | CHARIOTS CONSPIRACY         |
| MICHAEL     | DYING MAKER                 |
| MICHAEL     | ENOUGH RAGING               |
| MICHAEL     | GLASS DYING                 |
| MICHAEL     | HEAVENLY GUN                |
| MICHAEL     | HOMEWARD CIDER              |
| MICHAEL     | HOUSE DYNAMITE              |
| MICHAEL     | IDAHO LOVE                  |
| MICHAEL     | KARATE MOON                 |
| MICHAEL     | LAWLESS VISION              |
| MICHAEL     | LIAISONS SWEET              |
| MICHAEL     | MALKOVICH PET               |
| MICHAEL     | MARS ROMAN                  |
| MICHAEL     | METAL ARMAGEDDON            |
| MICHAEL     | MIXED DOORS                 |
| MICHAEL     | NOVOCAINE FLIGHT            |
| MICHAEL     | PATTON INTERVIEW            |
| MICHAEL     | PREJUDICE OLEANDER          |
| MICHAEL     | RIDGEMONT SUBMARINE         |
| MICHAEL     | SANTA PARIS                 |
| MICHAEL     | SOMETHING DUCK              |
| MICHAEL     | STEPMOM DREAM               |
| MICHAEL     | TELEMARK HEARTBREAKERS      |
| MICHAEL     | TENENBAUMS COMMAND          |
| MICHAEL     | TYCOON GATHERING            |
| MICHAEL     | UNBREAKABLE KARATE          |
| MICHAEL     | WATERSHIP FRONTIER          |
| MICHAEL     | WIFE TURN                   |
| JULIA       | BREAKFAST GOLDFINGER        |
| JULIA       | CRANES RESERVOIR            |
| JULIA       | DARES PLUTO                 |
| JULIA       | DETECTIVE VISION            |
| JULIA       | DIVORCE SHINING             |
| JULIA       | HOLLOW JEOPARDY             |
| JULIA       | JEOPARDY ENCINO             |
| JULIA       | LAMBS CINCINATTI            |
| JULIA       | MAJESTIC FLOATS             |
| JULIA       | MINDS TRUMAN                |
| JULIA       | OPEN AFRICAN                |
| JULIA       | OUTLAW HANKY                |
| JULIA       | PANKY SUBMARINE             |
| JULIA       | RIDER CADDYSHACK            |
| JULIA       | WON DARES                   |
| JULIA       | WYOMING STORM               |
| RENEE       | ALONE TRIP                  |
| RENEE       | ANGELS LIFE                 |
| RENEE       | ANTITRUST TOMATOES          |
| RENEE       | BALLOON HOMEWARD            |
| RENEE       | BINGO TALENTED              |
| RENEE       | BIRDCAGE CASPER             |
| RENEE       | BRIGHT ENCOUNTERS           |
| RENEE       | CABIN FLASH                 |
| RENEE       | CAT CONEHEADS               |
| RENEE       | COMANCHEROS ENEMY           |
| RENEE       | DESERT POSEIDON             |
| RENEE       | DESPERATE TRAINSPOTTING     |
| RENEE       | EXTRAORDINARY CONQUERER     |
| RENEE       | GHOST GROUNDHOG             |
| RENEE       | GREEDY ROOTS                |
| RENEE       | HILLS NEIGHBORS             |
| RENEE       | HOTEL HAPPINESS             |
| RENEE       | HUNTER ALTER                |
| RENEE       | JADE BUNCH                  |
| RENEE       | KING EVOLUTION              |
| RENEE       | LOVERBOY ATTACKS            |
| RENEE       | MAGNIFICENT CHITTY          |
| RENEE       | MASK PEACH                  |
| RENEE       | NATURAL STOCK               |
| RENEE       | NONE SPIKING                |
| RENEE       | PATRIOT ROMAN               |
| RENEE       | PERDITION FARGO             |
| RENEE       | SCARFACE BANG               |
| RENEE       | SENSE GREEK                 |
| RENEE       | TRAMP OTHERS                |
| RENEE       | TROUBLE DATE                |
| RENEE       | UNFAITHFUL KILL             |
| RENEE       | WIND PHANTOM                |
| ROCK        | ACADEMY DINOSAUR            |
| ROCK        | ALADDIN CALENDAR            |
| ROCK        | ALICE FANTASIA              |
| ROCK        | BALLOON HOMEWARD            |
| ROCK        | BUBBLE GROSSE               |
| ROCK        | CADDYSHACK JEDI             |
| ROCK        | CHITTY LOCK                 |
| ROCK        | DANCING FEVER               |
| ROCK        | DESIRE ALIEN                |
| ROCK        | EVE RESURRECTION            |
| ROCK        | FICTION CHRISTMAS           |
| ROCK        | FLATLINERS KILLER           |
| ROCK        | FRISCO FORREST              |
| ROCK        | HANGING DEEP                |
| ROCK        | HEAVYWEIGHTS BEAST          |
| ROCK        | LADY STAGE                  |
| ROCK        | LESSON CLEOPATRA            |
| ROCK        | LONELY ELEPHANT             |
| ROCK        | MAUDE MOD                   |
| ROCK        | MONTEREY LABYRINTH          |
| ROCK        | MUMMY CREATURES             |
| ROCK        | PATHS CONTROL               |
| ROCK        | SCISSORHANDS SLUMS          |
| ROCK        | SEABISCUIT PUNK             |
| ROCK        | SEARCHERS WAIT              |
| ROCK        | SNATCHERS MONTEZUMA         |
| ROCK        | STORM HAPPINESS             |
| ROCK        | UNITED PILOT                |
| ROCK        | WORKER TARZAN               |
| ROCK        | WORKING MICROCOSMOS         |
| CUBA        | ATLANTIS CAUSE              |
| CUBA        | BLOOD ARGONAUTS             |
| CUBA        | COMMANDMENTS EXPRESS        |
| CUBA        | DYNAMITE TARZAN             |
| CUBA        | EDGE KISSING                |
| CUBA        | FINDING ANACONDA            |
| CUBA        | GREATEST NORTH              |
| CUBA        | JUNGLE CLOSER               |
| CUBA        | LANGUAGE COWBOY             |
| CUBA        | LEAGUE HELLFIGHTERS         |
| CUBA        | LIBERTY MAGNIFICENT         |
| CUBA        | LOST BIRD                   |
| CUBA        | MAGNIFICENT CHITTY          |
| CUBA        | MARS ROMAN                  |
| CUBA        | NORTHWEST POLISH            |
| CUBA        | ROAD ROXANNE                |
| CUBA        | RUGRATS SHAKESPEARE         |
| CUBA        | SHIP WONDERLAND             |
| CUBA        | SONS INTERVIEW              |
| CUBA        | STRANGER STRANGERS          |
| CUBA        | TENENBAUMS COMMAND          |
| CUBA        | TOOTSIE PILOT               |
| CUBA        | TOWERS HURRICANE            |
| CUBA        | VICTORY ACADEMY             |
| AUDREY      | ARK RIDGEMONT               |
| AUDREY      | BANGER PINOCCHIO            |
| AUDREY      | BED HIGHBALL                |
| AUDREY      | BOONDOCK BALLROOM           |
| AUDREY      | CONFESSIONS MAGUIRE         |
| AUDREY      | DISTURBING SCARFACE         |
| AUDREY      | DRIFTER COMMANDMENTS        |
| AUDREY      | ELF MURDER                  |
| AUDREY      | FEVER EMPIRE                |
| AUDREY      | GRAFFITI LOVE               |
| AUDREY      | HEAVENLY GUN                |
| AUDREY      | HOME PITY                   |
| AUDREY      | ITALIAN AFRICAN             |
| AUDREY      | MAGNOLIA FORRESTER          |
| AUDREY      | MASKED BUBBLE               |
| AUDREY      | MUMMY CREATURES             |
| AUDREY      | NEWTON LABYRINTH            |
| AUDREY      | PILOT HOOSIERS              |
| AUDREY      | PITTSBURGH HUNCHBACK        |
| AUDREY      | POTTER CONNECTICUT          |
| AUDREY      | PRESIDENT BANG              |
| AUDREY      | PURPLE MOVIE                |
| AUDREY      | QUILLS BULL                 |
| AUDREY      | SKY MIRACLE                 |
| AUDREY      | SLEEPY JAPANESE             |
| AUDREY      | TADPOLE PARK                |
| AUDREY      | WARLOCK WEREWOLF            |
| GREGORY     | ALLEY EVOLUTION             |
| GREGORY     | ARMAGEDDON LOST             |
| GREGORY     | BOILED DARES                |
| GREGORY     | COWBOY DOOM                 |
| GREGORY     | DEEP CRUSADE                |
| GREGORY     | EXORCIST STING              |
| GREGORY     | EXPRESS LONELY              |
| GREGORY     | GREATEST NORTH              |
| GREGORY     | HEAVEN FREEDOM              |
| GREGORY     | HOLES BRANNIGAN             |
| GREGORY     | INSECTS STONE               |
| GREGORY     | MADISON TRAP                |
| GREGORY     | MAIDEN HOME                 |
| GREGORY     | MOONSHINE CABIN             |
| GREGORY     | OPERATION OPERATION         |
| GREGORY     | PEAK FOREVER                |
| GREGORY     | POTLUCK MIXED               |
| GREGORY     | SEATTLE EXPECATIONS         |
| GREGORY     | SISTER FREDDY               |
| GREGORY     | SONG HEDWIG                 |
| GREGORY     | SPICE SORORITY              |
| GREGORY     | SPIRIT FLINTSTONES          |
| GREGORY     | SPOILERS HELLFIGHTERS       |
| GREGORY     | STORM HAPPINESS             |
| GREGORY     | SUBMARINE BED               |
| GREGORY     | TROUBLE DATE                |
| GREGORY     | WARDROBE PHANTOM            |
| GREGORY     | WEST LION                   |
| GREGORY     | WHALE BIKINI                |
| GREGORY     | WRONG BEHAVIOR              |
| JOHN        | ALLEY EVOLUTION             |
| JOHN        | BEVERLY OUTLAW              |
| JOHN        | CANDLES GRAPES              |
| JOHN        | CLEOPATRA DEVIL             |
| JOHN        | COLOR PHILADELPHIA          |
| JOHN        | CONQUERER NUTS              |
| JOHN        | DAUGHTER MADIGAN            |
| JOHN        | GLEAMING JAWBREAKER         |
| JOHN        | GOLDMINE TYCOON             |
| JOHN        | HOME PITY                   |
| JOHN        | INTERVIEW LIAISONS          |
| JOHN        | ISHTAR ROCKETEER            |
| JOHN        | JAPANESE RUN                |
| JOHN        | JERSEY SASSY                |
| JOHN        | LUKE MUMMY                  |
| JOHN        | MILLION ACE                 |
| JOHN        | MONSTER SPARTACUS           |
| JOHN        | NAME DETECTIVE              |
| JOHN        | NECKLACE OUTBREAK           |
| JOHN        | NEWSIES STORY               |
| JOHN        | PET HAUNTING                |
| JOHN        | PIANIST OUTFIELD            |
| JOHN        | PINOCCHIO SIMON             |
| JOHN        | PITTSBURGH HUNCHBACK        |
| JOHN        | QUILLS BULL                 |
| JOHN        | RAGING AIRPLANE             |
| JOHN        | ROXANNE REBEL               |
| JOHN        | SATISFACTION CONFIDENTIAL   |
| JOHN        | SONG HEDWIG                 |
| BURT        | ATTACKS HATE                |
| BURT        | BLANKET BEVERLY             |
| BURT        | BUCKET BROTHERHOOD          |
| BURT        | BUTTERFLY CHOCOLAT          |
| BURT        | CAPER MOTIONS               |
| BURT        | CHICAGO NORTH               |
| BURT        | COAST RAINBOW               |
| BURT        | EVOLUTION ALTER             |
| BURT        | GATHERING CALENDAR          |
| BURT        | GILMORE BOILED              |
| BURT        | GRAPES FURY                 |
| BURT        | HEAVYWEIGHTS BEAST          |
| BURT        | INSIDER ARIZONA             |
| BURT        | POLLOCK DELIVERANCE         |
| BURT        | RACER EGG                   |
| BURT        | ROSES TREASURE              |
| BURT        | SLEUTH ORIENT               |
| BURT        | SPIKING ELEMENT             |
| BURT        | SPOILERS HELLFIGHTERS       |
| BURT        | STRAIGHT HOURS              |
| BURT        | VARSITY TRIP                |
| BURT        | WAIT CIDER                  |
| BURT        | WARS PLUTO                  |
| MERYL       | ALABAMA DEVIL               |
| MERYL       | ARTIST COLDBLOODED          |
| MERYL       | BERETS AGENT                |
| MERYL       | BOOGIE AMELIE               |
| MERYL       | BORN SPINAL                 |
| MERYL       | BRIGHT ENCOUNTERS           |
| MERYL       | CHANCE RESURRECTION         |
| MERYL       | CLUE GRAIL                  |
| MERYL       | CLYDE THEORY                |
| MERYL       | DAWN POND                   |
| MERYL       | DIRTY ACE                   |
| MERYL       | GATHERING CALENDAR          |
| MERYL       | HIGH ENCINO                 |
| MERYL       | JET NEIGHBORS               |
| MERYL       | KILLER INNOCENT             |
| MERYL       | LOSE INCH                   |
| MERYL       | RECORDS ZORRO               |
| MERYL       | ROCKETEER MOTHER            |
| MERYL       | SHEPHERD MIDSUMMER          |
| MERYL       | SWEET BROTHERHOOD           |
| MERYL       | VELVET TERMINATOR           |
| MERYL       | VICTORY ACADEMY             |
| JAYNE       | CAUSE DATE                  |
| JAYNE       | CELEBRITY HORN              |
| JAYNE       | CHICAGO NORTH               |
| JAYNE       | CHINATOWN GLADIATOR         |
| JAYNE       | EYES DRIVING                |
| JAYNE       | GLADIATOR WESTWARD          |
| JAYNE       | GLEAMING JAWBREAKER         |
| JAYNE       | HALL CASSIDY                |
| JAYNE       | HARRY IDAHO                 |
| JAYNE       | KARATE MOON                 |
| JAYNE       | LICENSE WEEKEND             |
| JAYNE       | LOUISIANA HARRY             |
| JAYNE       | MARS ROMAN                  |
| JAYNE       | MONSTER SPARTACUS           |
| JAYNE       | OZ LIAISONS                 |
| JAYNE       | PARIS WEEKEND               |
| JAYNE       | PERSONAL LADYBUGS           |
| JAYNE       | PIANIST OUTFIELD            |
| JAYNE       | QUEEN LUKE                  |
| JAYNE       | ROCKETEER MOTHER            |
| JAYNE       | SCHOOL JACKET               |
| JAYNE       | SEVEN SWARM                 |
| JAYNE       | SIDE ARK                    |
| JAYNE       | SMOOCHY CONTROL             |
| JAYNE       | SUSPECTS QUILLS             |
| JAYNE       | TEXAS WATCH                 |
| JAYNE       | WASTELAND DIVINE            |
| BELA        | BEETHOVEN EXORCIST          |
| BELA        | CARRIE BUNCH                |
| BELA        | CLERKS ANGELS               |
| BELA        | COMFORTS RUSH               |
| BELA        | ELEMENT FREDDY              |
| BELA        | ENEMY ODDS                  |
| BELA        | FANTASY TROOPERS            |
| BELA        | FLINTSTONES HAPPINESS       |
| BELA        | HOLLYWOOD ANONYMOUS         |
| BELA        | JACKET FRISCO               |
| BELA        | JERK PAYCHECK               |
| BELA        | LEGALLY SECRETARY           |
| BELA        | LION UNCUT                  |
| BELA        | LUKE MUMMY                  |
| BELA        | MARS ROMAN                  |
| BELA        | MIDSUMMER GROUNDHOG         |
| BELA        | MIGHTY LUCK                 |
| BELA        | MOD SECRETARY               |
| BELA        | NASH CHOCOLAT               |
| BELA        | OKLAHOMA JUMANJI            |
| BELA        | PIZZA JUMANJI               |
| BELA        | SIEGE MADRE                 |
| BELA        | SNATCHERS MONTEZUMA         |
| BELA        | SPLENDOR PATTON             |
| BELA        | STAGE WORLD                 |
| BELA        | TRAMP OTHERS                |
| BELA        | TRAP GUYS                   |
| BELA        | TYCOON GATHERING            |
| BELA        | VERTIGO NORTHWEST           |
| BELA        | WHISPERER GIANT             |
| REESE       | AGENT TRUMAN                |
| REESE       | ANTITRUST TOMATOES          |
| REESE       | BEDAZZLED MARRIED           |
| REESE       | CASABLANCA SUPER            |
| REESE       | CAUSE DATE                  |
| REESE       | CHOCOLAT HARRY              |
| REESE       | COAST RAINBOW               |
| REESE       | CREATURES SHAKESPEARE       |
| REESE       | DOORS PRESIDENT             |
| REESE       | DRACULA CRYSTAL             |
| REESE       | DRUMS DYNAMITE              |
| REESE       | GODFATHER DIARY             |
| REESE       | GOODFELLAS SALUTE           |
| REESE       | GORGEOUS BINGO              |
| REESE       | HOBBIT ALIEN                |
| REESE       | LIFE TWISTED                |
| REESE       | LOSE INCH                   |
| REESE       | MALKOVICH PET               |
| REESE       | MOSQUITO ARMAGEDDON         |
| REESE       | NORTHWEST POLISH            |
| REESE       | POSEIDON FOREVER            |
| REESE       | REMEMBER DIARY              |
| REESE       | ROUGE SQUAD                 |
| REESE       | RUNNER MADIGAN              |
| REESE       | SAINTS BRIDE                |
| REESE       | SCHOOL JACKET               |
| REESE       | SNATCHERS MONTEZUMA         |
| REESE       | TURN STAR                   |
| REESE       | VOLUME HOUSE                |
| REESE       | WEEKEND PERSONAL            |
| REESE       | WILD APOLLO                 |
| REESE       | WITCHES PANIC               |
| REESE       | YENTL IDAHO                 |
| MARY        | ACADEMY DINOSAUR            |
| MARY        | BUTTERFLY CHOCOLAT          |
| MARY        | CASSIDY WYOMING             |
| MARY        | CRAFT OUTFIELD              |
| MARY        | DUMBO LUST                  |
| MARY        | DWARFS ALTER                |
| MARY        | FANTASY TROOPERS            |
| MARY        | FEUD FROGMEN                |
| MARY        | FICTION CHRISTMAS           |
| MARY        | FORREST SONS                |
| MARY        | GAMES BOWFINGER             |
| MARY        | GREEDY ROOTS                |
| MARY        | HANDICAP BOONDOCK           |
| MARY        | HAUNTING PIANIST            |
| MARY        | IDOLS SNATCHERS             |
| MARY        | INTENTIONS EMPIRE           |
| MARY        | JEOPARDY ENCINO             |
| MARY        | KING EVOLUTION              |
| MARY        | LOVELY JINGLE               |
| MARY        | LUKE MUMMY                  |
| MARY        | MADNESS ATTACKS             |
| MARY        | MALLRATS UNITED             |
| MARY        | MEMENTO ZOOLANDER           |
| MARY        | MERMAID INSECTS             |
| MARY        | MODEL FISH                  |
| MARY        | MOONWALKER FOOL             |
| MARY        | NORTHWEST POLISH            |
| MARY        | ROSES TREASURE              |
| MARY        | SAINTS BRIDE                |
| MARY        | SIERRA DIVIDE               |
| MARY        | SLEEPY JAPANESE             |
| MARY        | SOLDIERS EVOLUTION          |
| MARY        | STEEL SANTA                 |
| MARY        | SUBMARINE BED               |
| MARY        | SWEDEN SHINING              |
| MARY        | THEORY MERMAID              |
| MARY        | TITANIC BOONDOCK            |
| MARY        | UNFORGIVEN ZOOLANDER        |
| MARY        | WAGON JAWS                  |
| MARY        | YOUTH KICK                  |
| JULIA       | BERETS AGENT                |
| JULIA       | BOILED DARES                |
| JULIA       | CHISUM BEHAVIOR             |
| JULIA       | CLOSER BANG                 |
| JULIA       | DAY UNFAITHFUL              |
| JULIA       | HOPE TOOTSIE                |
| JULIA       | LUKE MUMMY                  |
| JULIA       | MULAN MOON                  |
| JULIA       | OPUS ICE                    |
| JULIA       | POLLOCK DELIVERANCE         |
| JULIA       | RIDGEMONT SUBMARINE         |
| JULIA       | SHANGHAI TYCOON             |
| JULIA       | SHAWSHANK BUBBLE            |
| JULIA       | THEORY MERMAID              |
| JULIA       | WAIT CIDER                  |
| THORA       | AFRICAN EGG                 |
| THORA       | BADMAN DAWN                 |
| THORA       | BLANKET BEVERLY             |
| THORA       | CANDIDATE PERDITION         |
| THORA       | CAROL TEXAS                 |
| THORA       | CHRISTMAS MOONSHINE         |
| THORA       | GALAXY SWEETHEARTS          |
| THORA       | HOCUS FRIDA                 |
| THORA       | INSIDER ARIZONA             |
| THORA       | INTERVIEW LIAISONS          |
| THORA       | JADE BUNCH                  |
| THORA       | LOVER TRUMAN                |
| THORA       | LOVERBOY ATTACKS            |
| THORA       | MADISON TRAP                |
| THORA       | RANDOM GO                   |
| THORA       | TELEGRAPH VOYAGE            |
| THORA       | TROJAN TOMORROW             |
| THORA       | VIRGINIAN PLUTO             |
| THORA       | WARDROBE PHANTOM            |
| THORA       | WRONG BEHAVIOR              |
+-------------+-----------------------------+
5462 rows in set (0,01 sec)
   ```

2. Listar todos los clientes y los almacenes donde están
registrados.

```mysql
select c.nombre, c.apellidos, a.id_almacen
from cliente as c
left join almacen as a ON a.id_almacen = c.id_almacen;   
select c.nombre, c.apellidos, a.id_almacen
from cliente as c
left join almacen as a ON a.id_almacen = c.id_almacen;
+-------------+--------------+------------+
| nombre      | apellidos    | id_almacen |
+-------------+--------------+------------+
| MARY        | SMITH        |          1 |
| PATRICIA    | JOHNSON      |          1 |
| LINDA       | WILLIAMS     |          1 |
| BARBARA     | JONES        |          2 |
| ELIZABETH   | BROWN        |          1 |
| JENNIFER    | DAVIS        |          2 |
| MARIA       | MILLER       |          1 |
| SUSAN       | WILSON       |          2 |
| MARGARET    | MOORE        |          2 |
| DOROTHY     | TAYLOR       |          1 |
| LISA        | ANDERSON     |          2 |
| NANCY       | THOMAS       |          1 |
| KAREN       | JACKSON      |          2 |
| BETTY       | WHITE        |          2 |
| HELEN       | HARRIS       |          1 |
| SANDRA      | MARTIN       |          2 |
| DONNA       | THOMPSON     |          1 |
| CAROL       | GARCIA       |          2 |
| RUTH        | MARTINEZ     |          1 |
| SHARON      | ROBINSON     |          2 |
| MICHELLE    | CLARK        |          1 |
| LAURA       | RODRIGUEZ    |          1 |
| SARAH       | LEWIS        |          2 |
| KIMBERLY    | LEE          |          2 |
| DEBORAH     | WALKER       |          1 |
| JESSICA     | HALL         |          2 |
| SHIRLEY     | ALLEN        |          2 |
| CYNTHIA     | YOUNG        |          1 |
| ANGELA      | HERNANDEZ    |          2 |
| MELISSA     | KING         |          1 |
| BRENDA      | WRIGHT       |          2 |
| AMY         | LOPEZ        |          1 |
| ANNA        | HILL         |          2 |
| REBECCA     | SCOTT        |          2 |
| VIRGINIA    | GREEN        |          2 |
| KATHLEEN    | ADAMS        |          2 |
| PAMELA      | BAKER        |          1 |
| MARTHA      | GONZALEZ     |          1 |
| DEBRA       | NELSON       |          1 |
| AMANDA      | CARTER       |          2 |
| STEPHANIE   | MITCHELL     |          1 |
| CAROLYN     | PEREZ        |          2 |
| CHRISTINE   | ROBERTS      |          2 |
| MARIE       | TURNER       |          1 |
| JANET       | PHILLIPS     |          1 |
| CATHERINE   | CAMPBELL     |          2 |
| FRANCES     | PARKER       |          1 |
| ANN         | EVANS        |          1 |
| JOYCE       | EDWARDS      |          2 |
| DIANE       | COLLINS      |          1 |
| ALICE       | STEWART      |          1 |
| JULIE       | SANCHEZ      |          1 |
| HEATHER     | MORRIS       |          1 |
| TERESA      | ROGERS       |          1 |
| DORIS       | REED         |          2 |
| GLORIA      | COOK         |          1 |
| EVELYN      | MORGAN       |          2 |
| JEAN        | BELL         |          1 |
| CHERYL      | MURPHY       |          1 |
| MILDRED     | BAILEY       |          1 |
| KATHERINE   | RIVERA       |          2 |
| JOAN        | COOPER       |          1 |
| ASHLEY      | RICHARDSON   |          1 |
| JUDITH      | COX          |          2 |
| ROSE        | HOWARD       |          2 |
| JANICE      | WARD         |          2 |
| KELLY       | TORRES       |          1 |
| NICOLE      | PETERSON     |          1 |
| JUDY        | GRAY         |          2 |
| CHRISTINA   | RAMIREZ      |          2 |
| KATHY       | JAMES        |          1 |
| THERESA     | WATSON       |          2 |
| BEVERLY     | BROOKS       |          2 |
| DENISE      | KELLY        |          1 |
| TAMMY       | SANDERS      |          2 |
| IRENE       | PRICE        |          2 |
| JANE        | BENNETT      |          2 |
| LORI        | WOOD         |          1 |
| RACHEL      | BARNES       |          1 |
| MARILYN     | ROSS         |          1 |
| ANDREA      | HENDERSON    |          1 |
| KATHRYN     | COLEMAN      |          1 |
| LOUISE      | JENKINS      |          1 |
| SARA        | PERRY        |          2 |
| ANNE        | POWELL       |          2 |
| JACQUELINE  | LONG         |          2 |
| WANDA       | PATTERSON    |          1 |
| BONNIE      | HUGHES       |          2 |
| JULIA       | FLORES       |          1 |
| RUBY        | WASHINGTON   |          2 |
| LOIS        | BUTLER       |          2 |
| TINA        | SIMMONS      |          2 |
| PHYLLIS     | FOSTER       |          1 |
| NORMA       | GONZALES     |          1 |
| PAULA       | BRYANT       |          2 |
| DIANA       | ALEXANDER    |          1 |
| ANNIE       | RUSSELL      |          2 |
| LILLIAN     | GRIFFIN      |          1 |
| EMILY       | DIAZ         |          2 |
| ROBIN       | HAYES        |          1 |
| PEGGY       | MYERS        |          1 |
| CRYSTAL     | FORD         |          1 |
| GLADYS      | HAMILTON     |          1 |
| RITA        | GRAHAM       |          1 |
| DAWN        | SULLIVAN     |          1 |
| CONNIE      | WALLACE      |          1 |
| FLORENCE    | WOODS        |          1 |
| TRACY       | COLE         |          1 |
| EDNA        | WEST         |          2 |
| TIFFANY     | JORDAN       |          2 |
| CARMEN      | OWENS        |          1 |
| ROSA        | REYNOLDS     |          2 |
| CINDY       | FISHER       |          2 |
| GRACE       | ELLIS        |          2 |
| WENDY       | HARRISON     |          1 |
| VICTORIA    | GIBSON       |          1 |
| EDITH       | MCDONALD     |          1 |
| KIM         | CRUZ         |          1 |
| SHERRY      | MARSHALL     |          1 |
| SYLVIA      | ORTIZ        |          2 |
| JOSEPHINE   | GOMEZ        |          1 |
| THELMA      | MURRAY       |          1 |
| SHANNON     | FREEMAN      |          2 |
| SHEILA      | WELLS        |          1 |
| ETHEL       | WEBB         |          1 |
| ELLEN       | SIMPSON      |          1 |
| ELAINE      | STEVENS      |          2 |
| MARJORIE    | TUCKER       |          1 |
| CARRIE      | PORTER       |          1 |
| CHARLOTTE   | HUNTER       |          1 |
| MONICA      | HICKS        |          2 |
| ESTHER      | CRAWFORD     |          2 |
| PAULINE     | HENRY        |          1 |
| EMMA        | BOYD         |          1 |
| JUANITA     | MASON        |          2 |
| ANITA       | MORALES      |          2 |
| RHONDA      | KENNEDY      |          2 |
| HAZEL       | WARREN       |          1 |
| AMBER       | DIXON        |          1 |
| EVA         | RAMOS        |          1 |
| DEBBIE      | REYES        |          1 |
| APRIL       | BURNS        |          1 |
| LESLIE      | GORDON       |          1 |
| CLARA       | SHAW         |          1 |
| LUCILLE     | HOLMES       |          1 |
| JAMIE       | RICE         |          1 |
| JOANNE      | ROBERTSON    |          2 |
| ELEANOR     | HUNT         |          1 |
| VALERIE     | BLACK        |          1 |
| DANIELLE    | DANIELS      |          2 |
| MEGAN       | PALMER       |          2 |
| ALICIA      | MILLS        |          1 |
| SUZANNE     | NICHOLS      |          2 |
| MICHELE     | GRANT        |          2 |
| GAIL        | KNIGHT       |          1 |
| BERTHA      | FERGUSON     |          1 |
| DARLENE     | ROSE         |          2 |
| VERONICA    | STONE        |          1 |
| JILL        | HAWKINS      |          1 |
| ERIN        | DUNN         |          2 |
| GERALDINE   | PERKINS      |          1 |
| LAUREN      | HUDSON       |          2 |
| CATHY       | SPENCER      |          1 |
| JOANN       | GARDNER      |          2 |
| LORRAINE    | STEPHENS     |          2 |
| LYNN        | PAYNE        |          1 |
| SALLY       | PIERCE       |          2 |
| REGINA      | BERRY        |          1 |
| ERICA       | MATTHEWS     |          2 |
| BEATRICE    | ARNOLD       |          1 |
| DOLORES     | WAGNER       |          2 |
| BERNICE     | WILLIS       |          1 |
| AUDREY      | RAY          |          1 |
| YVONNE      | WATKINS      |          2 |
| ANNETTE     | OLSON        |          1 |
| JUNE        | CARROLL      |          1 |
| SAMANTHA    | DUNCAN       |          2 |
| MARION      | SNYDER       |          2 |
| DANA        | HART         |          1 |
| STACY       | CUNNINGHAM   |          2 |
| ANA         | BRADLEY      |          2 |
| RENEE       | LANE         |          1 |
| IDA         | ANDREWS      |          2 |
| VIVIAN      | RUIZ         |          1 |
| ROBERTA     | HARPER       |          1 |
| HOLLY       | FOX          |          2 |
| BRITTANY    | RILEY        |          2 |
| MELANIE     | ARMSTRONG    |          1 |
| LORETTA     | CARPENTER    |          1 |
| YOLANDA     | WEAVER       |          2 |
| JEANETTE    | GREENE       |          1 |
| LAURIE      | LAWRENCE     |          1 |
| KATIE       | ELLIOTT      |          2 |
| KRISTEN     | CHAVEZ       |          2 |
| VANESSA     | SIMS         |          1 |
| ALMA        | AUSTIN       |          1 |
| SUE         | PETERS       |          2 |
| ELSIE       | KELLEY       |          2 |
| BETH        | FRANKLIN     |          2 |
| JEANNE      | LAWSON       |          2 |
| VICKI       | FIELDS       |          1 |
| CARLA       | GUTIERREZ    |          2 |
| TARA        | RYAN         |          1 |
| ROSEMARY    | SCHMIDT      |          1 |
| EILEEN      | CARR         |          2 |
| TERRI       | VASQUEZ      |          1 |
| GERTRUDE    | CASTILLO     |          1 |
| LUCY        | WHEELER      |          1 |
| TONYA       | CHAPMAN      |          2 |
| ELLA        | OLIVER       |          2 |
| STACEY      | MONTGOMERY   |          1 |
| WILMA       | RICHARDS     |          2 |
| GINA        | WILLIAMSON   |          1 |
| KRISTIN     | JOHNSTON     |          1 |
| JESSIE      | BANKS        |          2 |
| NATALIE     | MEYER        |          1 |
| AGNES       | BISHOP       |          2 |
| VERA        | MCCOY        |          1 |
| WILLIE      | HOWELL       |          2 |
| CHARLENE    | ALVAREZ      |          2 |
| BESSIE      | MORRISON     |          1 |
| DELORES     | HANSEN       |          2 |
| MELINDA     | FERNANDEZ    |          1 |
| PEARL       | GARZA        |          2 |
| ARLENE      | HARVEY       |          1 |
| MAUREEN     | LITTLE       |          2 |
| COLLEEN     | BURTON       |          1 |
| ALLISON     | STANLEY      |          2 |
| TAMARA      | NGUYEN       |          1 |
| JOY         | GEORGE       |          2 |
| GEORGIA     | JACOBS       |          1 |
| CONSTANCE   | REID         |          2 |
| LILLIE      | KIM          |          2 |
| CLAUDIA     | FULLER       |          1 |
| JACKIE      | LYNCH        |          1 |
| MARCIA      | DEAN         |          1 |
| TANYA       | GILBERT      |          1 |
| NELLIE      | GARRETT      |          1 |
| MINNIE      | ROMERO       |          2 |
| MARLENE     | WELCH        |          1 |
| HEIDI       | LARSON       |          2 |
| GLENDA      | FRAZIER      |          1 |
| LYDIA       | BURKE        |          1 |
| VIOLA       | HANSON       |          2 |
| COURTNEY    | DAY          |          1 |
| MARIAN      | MENDOZA      |          1 |
| STELLA      | MORENO       |          1 |
| CAROLINE    | BOWMAN       |          1 |
| DORA        | MEDINA       |          2 |
| JO          | FOWLER       |          2 |
| VICKIE      | BREWER       |          2 |
| MATTIE      | HOFFMAN      |          2 |
| TERRY       | CARLSON      |          1 |
| MAXINE      | SILVA        |          2 |
| IRMA        | PEARSON      |          2 |
| MABEL       | HOLLAND      |          2 |
| MARSHA      | DOUGLAS      |          2 |
| MYRTLE      | FLEMING      |          1 |
| LENA        | JENSEN       |          2 |
| CHRISTY     | VARGAS       |          1 |
| DEANNA      | BYRD         |          1 |
| PATSY       | DAVIDSON     |          2 |
| HILDA       | HOPKINS      |          1 |
| GWENDOLYN   | MAY          |          1 |
| JENNIE      | TERRY        |          2 |
| NORA        | HERRERA      |          2 |
| MARGIE      | WADE         |          1 |
| NINA        | SOTO         |          1 |
| CASSANDRA   | WALTERS      |          1 |
| LEAH        | CURTIS       |          1 |
| PENNY       | NEAL         |          1 |
| KAY         | CALDWELL     |          1 |
| PRISCILLA   | LOWE         |          2 |
| NAOMI       | JENNINGS     |          1 |
| CAROLE      | BARNETT      |          2 |
| BRANDY      | GRAVES       |          1 |
| OLGA        | JIMENEZ      |          2 |
| BILLIE      | HORTON       |          2 |
| DIANNE      | SHELTON      |          2 |
| TRACEY      | BARRETT      |          2 |
| LEONA       | OBRIEN       |          2 |
| JENNY       | CASTRO       |          2 |
| FELICIA     | SUTTON       |          1 |
| SONIA       | GREGORY      |          1 |
| MIRIAM      | MCKINNEY     |          1 |
| VELMA       | LUCAS        |          1 |
| BECKY       | MILES        |          2 |
| BOBBIE      | CRAIG        |          1 |
| VIOLET      | RODRIQUEZ    |          1 |
| KRISTINA    | CHAMBERS     |          1 |
| TONI        | HOLT         |          1 |
| MISTY       | LAMBERT      |          2 |
| MAE         | FLETCHER     |          2 |
| SHELLY      | WATTS        |          2 |
| DAISY       | BATES        |          1 |
| RAMONA      | HALE         |          2 |
| SHERRI      | RHODES       |          1 |
| ERIKA       | PENA         |          1 |
| JAMES       | GANNON       |          2 |
| JOHN        | FARNSWORTH   |          1 |
| ROBERT      | BAUGHMAN     |          2 |
| MICHAEL     | SILVERMAN    |          1 |
| WILLIAM     | SATTERFIELD  |          2 |
| DAVID       | ROYAL        |          2 |
| RICHARD     | MCCRARY      |          1 |
| CHARLES     | KOWALSKI     |          1 |
| JOSEPH      | JOY          |          2 |
| THOMAS      | GRIGSBY      |          1 |
| CHRISTOPHER | GRECO        |          1 |
| DANIEL      | CABRAL       |          2 |
| PAUL        | TROUT        |          2 |
| MARK        | RINEHART     |          2 |
| DONALD      | MAHON        |          2 |
| GEORGE      | LINTON       |          1 |
| KENNETH     | GOODEN       |          2 |
| STEVEN      | CURLEY       |          1 |
| EDWARD      | BAUGH        |          2 |
| BRIAN       | WYMAN        |          1 |
| RONALD      | WEINER       |          2 |
| ANTHONY     | SCHWAB       |          2 |
| KEVIN       | SCHULER      |          1 |
| JASON       | MORRISSEY    |          1 |
| MATTHEW     | MAHAN        |          2 |
| GARY        | COY          |          2 |
| TIMOTHY     | BUNN         |          1 |
| JOSE        | ANDREW       |          1 |
| LARRY       | THRASHER     |          2 |
| JEFFREY     | SPEAR        |          2 |
| FRANK       | WAGGONER     |          2 |
| SCOTT       | SHELLEY      |          1 |
| ERIC        | ROBERT       |          1 |
| STEPHEN     | QUALLS       |          1 |
| ANDREW      | PURDY        |          2 |
| RAYMOND     | MCWHORTER    |          2 |
| GREGORY     | MAULDIN      |          1 |
| JOSHUA      | MARK         |          1 |
| JERRY       | JORDON       |          1 |
| DENNIS      | GILMAN       |          1 |
| WALTER      | PERRYMAN     |          2 |
| PATRICK     | NEWSOM       |          1 |
| PETER       | MENARD       |          1 |
| HAROLD      | MARTINO      |          1 |
| DOUGLAS     | GRAF         |          1 |
| HENRY       | BILLINGSLEY  |          1 |
| CARL        | ARTIS        |          1 |
| ARTHUR      | SIMPKINS     |          1 |
| RYAN        | SALISBURY    |          2 |
| ROGER       | QUINTANILLA  |          2 |
| JOE         | GILLILAND    |          2 |
| JUAN        | FRALEY       |          1 |
| JACK        | FOUST        |          1 |
| ALBERT      | CROUSE       |          1 |
| JONATHAN    | SCARBOROUGH  |          1 |
| JUSTIN      | NGO          |          2 |
| TERRY       | GRISSOM      |          2 |
| GERALD      | FULTZ        |          2 |
| KEITH       | RICO         |          1 |
| SAMUEL      | MARLOW       |          2 |
| WILLIE      | MARKHAM      |          2 |
| RALPH       | MADRIGAL     |          2 |
| LAWRENCE    | LAWTON       |          2 |
| NICHOLAS    | BARFIELD     |          1 |
| ROY         | WHITING      |          2 |
| BENJAMIN    | VARNEY       |          1 |
| BRUCE       | SCHWARZ      |          2 |
| BRANDON     | HUEY         |          1 |
| ADAM        | GOOCH        |          1 |
| HARRY       | ARCE         |          1 |
| FRED        | WHEAT        |          2 |
| WAYNE       | TRUONG       |          2 |
| BILLY       | POULIN       |          1 |
| STEVE       | MACKENZIE    |          2 |
| LOUIS       | LEONE        |          1 |
| JEREMY      | HURTADO      |          2 |
| AARON       | SELBY        |          2 |
| RANDY       | GAITHER      |          1 |
| HOWARD      | FORTNER      |          1 |
| EUGENE      | CULPEPPER    |          1 |
| CARLOS      | COUGHLIN     |          1 |
| RUSSELL     | BRINSON      |          1 |
| BOBBY       | BOUDREAU     |          2 |
| VICTOR      | BARKLEY      |          2 |
| MARTIN      | BALES        |          1 |
| ERNEST      | STEPP        |          2 |
| PHILLIP     | HOLM         |          1 |
| TODD        | TAN          |          1 |
| JESSE       | SCHILLING    |          2 |
| CRAIG       | MORRELL      |          2 |
| ALAN        | KAHN         |          1 |
| SHAWN       | HEATON       |          1 |
| CLARENCE    | GAMEZ        |          1 |
| SEAN        | DOUGLASS     |          2 |
| PHILIP      | CAUSEY       |          1 |
| CHRIS       | BROTHERS     |          2 |
| JOHNNY      | TURPIN       |          2 |
| EARL        | SHANKS       |          1 |
| JIMMY       | SCHRADER     |          1 |
| ANTONIO     | MEEK         |          1 |
| DANNY       | ISOM         |          1 |
| BRYAN       | HARDISON     |          2 |
| TONY        | CARRANZA     |          2 |
| LUIS        | YANEZ        |          1 |
| MIKE        | WAY          |          1 |
| STANLEY     | SCROGGINS    |          2 |
| LEONARD     | SCHOFIELD    |          1 |
| NATHAN      | RUNYON       |          1 |
| DALE        | RATCLIFF     |          1 |
| MANUEL      | MURRELL      |          1 |
| RODNEY      | MOELLER      |          2 |
| CURTIS      | IRBY         |          2 |
| NORMAN      | CURRIER      |          1 |
| ALLEN       | BUTTERFIELD  |          2 |
| MARVIN      | YEE          |          2 |
| VINCENT     | RALSTON      |          1 |
| GLENN       | PULLEN       |          1 |
| JEFFERY     | PINSON       |          2 |
| TRAVIS      | ESTEP        |          1 |
| JEFF        | EAST         |          2 |
| CHAD        | CARBONE      |          1 |
| JACOB       | LANCE        |          1 |
| LEE         | HAWKS        |          1 |
| MELVIN      | ELLINGTON    |          1 |
| ALFRED      | CASILLAS     |          2 |
| KYLE        | SPURLOCK     |          2 |
| FRANCIS     | SIKES        |          2 |
| BRADLEY     | MOTLEY       |          1 |
| JESUS       | MCCARTNEY    |          2 |
| HERBERT     | KRUGER       |          2 |
| FREDERICK   | ISBELL       |          2 |
| RAY         | HOULE        |          1 |
| JOEL        | FRANCISCO    |          2 |
| EDWIN       | BURK         |          1 |
| DON         | BONE         |          1 |
| EDDIE       | TOMLIN       |          1 |
| RICKY       | SHELBY       |          2 |
| TROY        | QUIGLEY      |          1 |
| RANDALL     | NEUMANN      |          2 |
| BARRY       | LOVELACE     |          1 |
| ALEXANDER   | FENNELL      |          2 |
| BERNARD     | COLBY        |          1 |
| MARIO       | CHEATHAM     |          1 |
| LEROY       | BUSTAMANTE   |          1 |
| FRANCISCO   | SKIDMORE     |          2 |
| MARCUS      | HIDALGO      |          2 |
| MICHEAL     | FORMAN       |          1 |
| THEODORE    | CULP         |          2 |
| CLIFFORD    | BOWENS       |          1 |
| MIGUEL      | BETANCOURT   |          1 |
| OSCAR       | AQUINO       |          2 |
| JAY         | ROBB         |          1 |
| JIM         | REA          |          1 |
| TOM         | MILNER       |          1 |
| CALVIN      | MARTEL       |          1 |
| ALEX        | GRESHAM      |          2 |
| JON         | WILES        |          2 |
| RONNIE      | RICKETTS     |          2 |
| BILL        | GAVIN        |          2 |
| LLOYD       | DOWD         |          1 |
| TOMMY       | COLLAZO      |          1 |
| LEON        | BOSTIC       |          1 |
| DEREK       | BLAKELY      |          1 |
| WARREN      | SHERROD      |          2 |
| DARRELL     | POWER        |          2 |
| JEROME      | KENYON       |          1 |
| FLOYD       | GANDY        |          1 |
| LEO         | EBERT        |          1 |
| ALVIN       | DELOACH      |          2 |
| TIM         | CARY         |          1 |
| WESLEY      | BULL         |          2 |
| GORDON      | ALLARD       |          1 |
| DEAN        | SAUER        |          1 |
| GREG        | ROBINS       |          1 |
| JORGE       | OLIVARES     |          2 |
| DUSTIN      | GILLETTE     |          2 |
| PEDRO       | CHESTNUT     |          2 |
| DERRICK     | BOURQUE      |          1 |
| DAN         | PAINE        |          1 |
| LEWIS       | LYMAN        |          1 |
| ZACHARY     | HITE         |          1 |
| COREY       | HAUSER       |          1 |
| HERMAN      | DEVORE       |          1 |
| MAURICE     | CRAWLEY      |          1 |
| VERNON      | CHAPA        |          2 |
| ROBERTO     | VU           |          1 |
| CLYDE       | TOBIAS       |          1 |
| GLEN        | TALBERT      |          1 |
| HECTOR      | POINDEXTER   |          2 |
| SHANE       | MILLARD      |          2 |
| RICARDO     | MEADOR       |          1 |
| SAM         | MCDUFFIE     |          1 |
| RICK        | MATTOX       |          2 |
| LESTER      | KRAUS        |          2 |
| BRENT       | HARKINS      |          1 |
| RAMON       | CHOATE       |          2 |
| CHARLIE     | BESS         |          2 |
| TYLER       | WREN         |          2 |
| GILBERT     | SLEDGE       |          2 |
| GENE        | SANBORN      |          1 |
| MARC        | OUTLAW       |          2 |
| REGINALD    | KINDER       |          1 |
| RUBEN       | GEARY        |          1 |
| BRETT       | CORNWELL     |          1 |
| ANGEL       | BARCLAY      |          1 |
| NATHANIEL   | ADAM         |          1 |
| RAFAEL      | ABNEY        |          1 |
| LESLIE      | SEWARD       |          2 |
| EDGAR       | RHOADS       |          2 |
| MILTON      | HOWLAND      |          2 |
| RAUL        | FORTIER      |          1 |
| BEN         | EASTER       |          2 |
| CHESTER     | BENNER       |          1 |
| CECIL       | VINES        |          1 |
| DUANE       | TUBBS        |          2 |
| FRANKLIN    | TROUTMAN     |          2 |
| ANDRE       | RAPP         |          1 |
| ELMER       | NOE          |          2 |
| BRAD        | MCCURDY      |          2 |
| GABRIEL     | HARDER       |          1 |
| RON         | DELUCA       |          2 |
| MITCHELL    | WESTMORELAND |          2 |
| ROLAND      | SOUTH        |          2 |
| ARNOLD      | HAVENS       |          2 |
| HARVEY      | GUAJARDO     |          1 |
| JARED       | ELY          |          1 |
| ADRIAN      | CLARY        |          2 |
| KARL        | SEAL         |          2 |
| CORY        | MEEHAN       |          1 |
| CLAUDE      | HERZOG       |          1 |
| ERIK        | GUILLEN      |          2 |
| DARRYL      | ASHCRAFT     |          2 |
| JAMIE       | WAUGH        |          2 |
| NEIL        | RENNER       |          2 |
| JESSIE      | MILAM        |          1 |
| CHRISTIAN   | JUNG         |          1 |
| JAVIER      | ELROD        |          1 |
| FERNANDO    | CHURCHILL    |          2 |
| CLINTON     | BUFORD       |          2 |
| TED         | BREAUX       |          2 |
| MATHEW      | BOLIN        |          1 |
| TYRONE      | ASHER        |          1 |
| DARREN      | WINDHAM      |          2 |
| LONNIE      | TIRADO       |          2 |
| LANCE       | PEMBERTON    |          1 |
| CODY        | NOLEN        |          2 |
| JULIO       | NOLAND       |          2 |
| KELLY       | KNOTT        |          1 |
| KURT        | EMMONS       |          1 |
| ALLAN       | CORNISH      |          1 |
| NELSON      | CHRISTENSON  |          1 |
| GUY         | BROWNLEE     |          2 |
| CLAYTON     | BARBEE       |          2 |
| HUGH        | WALDROP      |          2 |
| MAX         | PITT         |          1 |
| DWAYNE      | OLVERA       |          1 |
| DWIGHT      | LOMBARDI     |          1 |
| ARMANDO     | GRUBER       |          2 |
| FELIX       | GAFFNEY      |          1 |
| JIMMIE      | EGGLESTON    |          1 |
| EVERETT     | BANDA        |          2 |
| JORDAN      | ARCHULETA    |          1 |
| IAN         | STILL        |          2 |
| WALLACE     | SLONE        |          1 |
| KEN         | PREWITT      |          2 |
| BOB         | PFEIFFER     |          2 |
| JAIME       | NETTLES      |          2 |
| CASEY       | MENA         |          1 |
| ALFREDO     | MCADAMS      |          2 |
| ALBERTO     | HENNING      |          2 |
| DAVE        | GARDINER     |          2 |
| IVAN        | CROMWELL     |          2 |
| JOHNNIE     | CHISHOLM     |          2 |
| SIDNEY      | BURLESON     |          1 |
| BYRON       | BOX          |          1 |
| JULIAN      | VEST         |          2 |
| ISAAC       | OGLESBY      |          2 |
| MORRIS      | MCCARTER     |          2 |
| CLIFTON     | MALCOLM      |          2 |
| WILLARD     | LUMPKIN      |          2 |
| DARYL       | LARUE        |          2 |
| ROSS        | GREY         |          1 |
| VIRGIL      | WOFFORD      |          1 |
| ANDY        | VANHORN      |          2 |
| MARSHALL    | THORN        |          1 |
| SALVADOR    | TEEL         |          2 |
| PERRY       | SWAFFORD     |          1 |
| KIRK        | STCLAIR      |          1 |
| SERGIO      | STANFIELD    |          1 |
| MARION      | OCAMPO       |          1 |
| TRACY       | HERRMANN     |          1 |
| SETH        | HANNON       |          2 |
| KENT        | ARSENAULT    |          1 |
| TERRANCE    | ROUSH        |          1 |
| RENE        | MCALISTER    |          2 |
| EDUARDO     | HIATT        |          1 |
| TERRENCE    | GUNDERSON    |          1 |
| ENRIQUE     | FORSYTHE     |          1 |
| FREDDIE     | DUGGAN       |          1 |
| WADE        | DELVALLE     |          1 |
| AUSTIN      | CINTRON      |          2 |
| PEPE        | LÓPEZ        |          2 |
| MARÍA       | SÁNCHEZ      |          2 |
+-------------+--------------+------------+
601 rows in set (0,00 sec)

   ```


3. Encontrar todas las películas y sus respectivas categorías.

```mysql
select p.titulo, c.nombre as categoria
from pelicula as p
inner join pelicula_categoria as pc ON pc.id_pelicula = p.id_pelicula
inner join categoria as c ON c.id_categoria = pc.id_categoria;   

+-----------------------------+-------------+
| titulo                      | categoria   |
+-----------------------------+-------------+
| AMADEUS HOLY                | Action      |
| AMERICAN CIRCUS             | Action      |
| ANTITRUST TOMATOES          | Action      |
| ARK RIDGEMONT               | Action      |
| BAREFOOT MANCHURIAN         | Action      |
| BERETS AGENT                | Action      |
| BRIDE INTRIGUE              | Action      |
| BULL SHAWSHANK              | Action      |
| CADDYSHACK JEDI             | Action      |
| CAMPUS REMEMBER             | Action      |
| CASUALTIES ENCINO           | Action      |
| CELEBRITY HORN              | Action      |
| CLUELESS BUCKET             | Action      |
| CROW GREASE                 | Action      |
| DANCES NONE                 | Action      |
| DARKO DORADO                | Action      |
| DARN FORRESTER              | Action      |
| DEVIL DESIRE                | Action      |
| DRAGON SQUAD                | Action      |
| DREAM PICKUP                | Action      |
| DRIFTER COMMANDMENTS        | Action      |
| EASY GLADIATOR              | Action      |
| ENTRAPMENT SATISFACTION     | Action      |
| EXCITEMENT EVE              | Action      |
| FANTASY TROOPERS            | Action      |
| FIREHOUSE VIETNAM           | Action      |
| FOOL MOCKINGBIRD            | Action      |
| FORREST SONS                | Action      |
| GLASS DYING                 | Action      |
| GOSFORD DONNIE              | Action      |
| GRAIL FRANKENSTEIN          | Action      |
| HANDICAP BOONDOCK           | Action      |
| HILLS NEIGHBORS             | Action      |
| KISSING DOLLS               | Action      |
| LAWRENCE LOVE               | Action      |
| LORD ARIZONA                | Action      |
| LUST LOCK                   | Action      |
| MAGNOLIA FORRESTER          | Action      |
| MIDNIGHT WESTWARD           | Action      |
| MINDS TRUMAN                | Action      |
| MOCKINGBIRD HOLLYWOOD       | Action      |
| MONTEZUMA COMMAND           | Action      |
| PARK CITIZEN                | Action      |
| PATRIOT ROMAN               | Action      |
| PRIMARY GLASS               | Action      |
| QUEST MUSSOLINI             | Action      |
| REAR TRADING                | Action      |
| RINGS HEARTBREAKERS         | Action      |
| RUGRATS SHAKESPEARE         | Action      |
| SHRUNK DIVINE               | Action      |
| SIDE ARK                    | Action      |
| SKY MIRACLE                 | Action      |
| SOUTH WAIT                  | Action      |
| SPEAKEASY DATE              | Action      |
| STAGECOACH ARMAGEDDON       | Action      |
| STORY SIDE                  | Action      |
| SUSPECTS QUILLS             | Action      |
| TRIP NEWTON                 | Action      |
| TRUMAN CRAZY                | Action      |
| UPRISING UPTOWN             | Action      |
| WATERFRONT DELIVERANCE      | Action      |
| WEREWOLF LOLA               | Action      |
| WOMEN DORADO                | Action      |
| WORST BANGER                | Action      |
| ALTER VICTORY               | Animation   |
| ANACONDA CONFESSIONS        | Animation   |
| ARGONAUTS TOWN              | Animation   |
| BIKINI BORROWERS            | Animation   |
| BLACKOUT PRIVATE            | Animation   |
| BORROWERS BEDAZZLED         | Animation   |
| CANYON STOCK                | Animation   |
| CAROL TEXAS                 | Animation   |
| CHAMPION FLATLINERS         | Animation   |
| CLASH FREDDY                | Animation   |
| CLUB GRAFFITI               | Animation   |
| CROSSROADS CASUALTIES       | Animation   |
| DARES PLUTO                 | Animation   |
| DESIRE ALIEN                | Animation   |
| DOGMA FAMILY                | Animation   |
| DONNIE ALLEY                | Animation   |
| DOORS PRESIDENT             | Animation   |
| DOUBLE WRATH                | Animation   |
| DUCK RACER                  | Animation   |
| EARLY HOME                  | Animation   |
| FALCON VOLUME               | Animation   |
| FIGHT JAWBREAKER            | Animation   |
| FLOATS GARDEN               | Animation   |
| FLYING HOOK                 | Animation   |
| FORRESTER COMANCHEROS       | Animation   |
| GANGS PRIDE                 | Animation   |
| GHOSTBUSTERS ELF            | Animation   |
| HARPER DYING                | Animation   |
| HOOK CHARIOTS               | Animation   |
| HORN WORKING                | Animation   |
| INCH JET                    | Animation   |
| INSECTS STONE               | Animation   |
| INTENTIONS EMPIRE           | Animation   |
| ISHTAR ROCKETEER            | Animation   |
| JUGGLER HARDLY              | Animation   |
| LAWLESS VISION              | Animation   |
| LUKE MUMMY                  | Animation   |
| MASSAGE IMAGE               | Animation   |
| MENAGERIE RUSHMORE          | Animation   |
| MIRACLE VIRTUAL             | Animation   |
| MISSION ZOOLANDER           | Animation   |
| NASH CHOCOLAT               | Animation   |
| OSCAR GOLD                  | Animation   |
| OZ LIAISONS                 | Animation   |
| PACKER MADIGAN              | Animation   |
| POND SEATTLE                | Animation   |
| POTLUCK MIXED               | Animation   |
| POTTER CONNECTICUT          | Animation   |
| PRIDE ALAMO                 | Animation   |
| PUNK DIVORCE                | Animation   |
| ROOM ROMAN                  | Animation   |
| SLEEPLESS MONSOON           | Animation   |
| SNOWMAN ROLLERCOASTER       | Animation   |
| SONS INTERVIEW              | Animation   |
| STORM HAPPINESS             | Animation   |
| SUGAR WONKA                 | Animation   |
| SUNRISE LEAGUE              | Animation   |
| TELEMARK HEARTBREAKERS      | Animation   |
| THEORY MERMAID              | Animation   |
| THIEF PELICAN               | Animation   |
| TITANIC BOONDOCK            | Animation   |
| TRACY CIDER                 | Animation   |
| TURN STAR                   | Animation   |
| WAIT CIDER                  | Animation   |
| WATCH TRACY                 | Animation   |
| WONKA SEA                   | Animation   |
| BACKLASH UNDEFEATED         | Children    |
| BEAR GRACELAND              | Children    |
| BENEATH RUSH                | Children    |
| BETRAYED REAR               | Children    |
| CABIN FLASH                 | Children    |
| CASPER DRAGONFLY            | Children    |
| CHRISTMAS MOONSHINE         | Children    |
| CIRCUS YOUTH                | Children    |
| CLOCKWORK PARADISE          | Children    |
| COMANCHEROS ENEMY           | Children    |
| CROOKED FROGMEN             | Children    |
| DAUGHTER MADIGAN            | Children    |
| DOCTOR GRAIL                | Children    |
| EMPIRE MALKOVICH            | Children    |
| FARGO GANDHI                | Children    |
| FOREVER CANDIDATE           | Children    |
| FULL FLATLINERS             | Children    |
| FURY MURDER                 | Children    |
| GHOST GROUNDHOG             | Children    |
| GIANT TROOPERS              | Children    |
| GORGEOUS BINGO              | Children    |
| GRADUATE LORD               | Children    |
| HALL CASSIDY                | Children    |
| HEARTBREAKERS BRIGHT        | Children    |
| HOLLYWOOD ANONYMOUS         | Children    |
| HOLOCAUST HIGHBALL          | Children    |
| IDOLS SNATCHERS             | Children    |
| INVASION CYCLONE            | Children    |
| JERSEY SASSY                | Children    |
| JUMPING WRATH               | Children    |
| LABYRINTH LEAGUE            | Children    |
| LANGUAGE COWBOY             | Children    |
| LEGALLY SECRETARY           | Children    |
| MAGIC MALLRATS              | Children    |
| MAKER GABLES                | Children    |
| MICROCOSMOS PARADISE        | Children    |
| MODEL FISH                  | Children    |
| MURDER ANTITRUST            | Children    |
| NOON PAPI                   | Children    |
| POLISH BROOKLYN             | Children    |
| ROBBERS JOON                | Children    |
| SABRINA MIDNIGHT            | Children    |
| SANTA PARIS                 | Children    |
| SCARFACE BANG               | Children    |
| SHEPHERD MIDSUMMER          | Children    |
| SISTER FREDDY               | Children    |
| SPLENDOR PATTON             | Children    |
| STRANGELOVE DESIRE          | Children    |
| STRANGER STRANGERS          | Children    |
| SUNDANCE INVASION           | Children    |
| SWEETHEARTS SUSPECTS        | Children    |
| TEQUILA PAST                | Children    |
| TIES HUNGER                 | Children    |
| TOOTSIE PILOT               | Children    |
| TWISTED PIRATES             | Children    |
| UPTOWN YOUNG                | Children    |
| WALLS ARTIST                | Children    |
| WARLOCK WEREWOLF            | Children    |
| WRONG BEHAVIOR              | Children    |
| ZOOLANDER FICTION           | Children    |
| ALICE FANTASIA              | Classics    |
| ARIZONA BANG                | Classics    |
| BEAST HUNCHBACK             | Classics    |
| BOUND CHEAPER               | Classics    |
| CANDIDATE PERDITION         | Classics    |
| CENTER DINOSAUR             | Classics    |
| COLOR PHILADELPHIA          | Classics    |
| CONSPIRACY SPIRIT           | Classics    |
| CORE SUIT                   | Classics    |
| CREEPERS KANE               | Classics    |
| CRUELTY UNFORGIVEN          | Classics    |
| DETECTIVE VISION            | Classics    |
| DRACULA CRYSTAL             | Classics    |
| DYNAMITE TARZAN             | Classics    |
| EXTRAORDINARY CONQUERER     | Classics    |
| FROST HEAD                  | Classics    |
| GALAXY SWEETHEARTS          | Classics    |
| GILBERT PELICAN             | Classics    |
| GILMORE BOILED              | Classics    |
| HOLY TADPOLE                | Classics    |
| HOPE TOOTSIE                | Classics    |
| HYDE DOCTOR                 | Classics    |
| IRON MOON                   | Classics    |
| ISLAND EXORCIST             | Classics    |
| JEEPERS WEDDING             | Classics    |
| JEOPARDY ENCINO             | Classics    |
| JERK PAYCHECK               | Classics    |
| JINGLE SAGEBRUSH            | Classics    |
| LEAGUE HELLFIGHTERS         | Classics    |
| LIGHTS DEER                 | Classics    |
| LOATHING LEGALLY            | Classics    |
| LOVELY JINGLE               | Classics    |
| LOVER TRUMAN                | Classics    |
| MAGNIFICENT CHITTY          | Classics    |
| MALKOVICH PET               | Classics    |
| MILLION ACE                 | Classics    |
| MUSKETEERS WAIT             | Classics    |
| OCTOBER SUBMARINE           | Classics    |
| PAJAMA JAWBREAKER           | Classics    |
| PATIENT SISTER              | Classics    |
| PREJUDICE OLEANDER          | Classics    |
| REQUIEM TYCOON              | Classics    |
| RIGHT CRANES                | Classics    |
| ROOTS REMEMBER              | Classics    |
| SLING LUKE                  | Classics    |
| SNATCHERS MONTEZUMA         | Classics    |
| SPIKING ELEMENT             | Classics    |
| STEEL SANTA                 | Classics    |
| SUMMER SCARFACE             | Classics    |
| TADPOLE PARK                | Classics    |
| TIMBERLAND SKY              | Classics    |
| TOMORROW HUSTLER            | Classics    |
| TOWERS HURRICANE            | Classics    |
| VOLUME HOUSE                | Classics    |
| VOYAGE LEGALLY              | Classics    |
| WASTELAND DIVINE            | Classics    |
| WESTWARD SEABISCUIT         | Classics    |
| AIRPLANE SIERRA             | Comedy      |
| ANTHEM LUKE                 | Comedy      |
| BRINGING HYSTERICAL         | Comedy      |
| CAPER MOTIONS               | Comedy      |
| CAT CONEHEADS               | Comedy      |
| CLOSER BANG                 | Comedy      |
| CONNECTION MICROCOSMOS      | Comedy      |
| CONTROL ANTHEM              | Comedy      |
| CRAZY HOME                  | Comedy      |
| DADDY PITTSBURGH            | Comedy      |
| DOOM DANCING                | Comedy      |
| DOWNHILL ENOUGH             | Comedy      |
| DYING MAKER                 | Comedy      |
| ELEMENT FREDDY              | Comedy      |
| FERRIS MOTHER               | Comedy      |
| FIREBALL PHILADELPHIA       | Comedy      |
| FLINTSTONES HAPPINESS       | Comedy      |
| FRANKENSTEIN STRANGER       | Comedy      |
| FREEDOM CLEOPATRA           | Comedy      |
| GOLD RIVER                  | Comedy      |
| GROUNDHOG UNCUT             | Comedy      |
| GUNFIGHT MOON               | Comedy      |
| HATE HANDICAP               | Comedy      |
| HEAVEN FREEDOM              | Comedy      |
| HEDWIG ALTER                | Comedy      |
| HURRICANE AFFAIR            | Comedy      |
| HUSTLER PARTY               | Comedy      |
| JAWS HARRY                  | Comedy      |
| KNOCK WARLOCK               | Comedy      |
| LIFE TWISTED                | Comedy      |
| LION UNCUT                  | Comedy      |
| LONELY ELEPHANT             | Comedy      |
| MALLRATS UNITED             | Comedy      |
| MEMENTO ZOOLANDER           | Comedy      |
| MULAN MOON                  | Comedy      |
| MYSTIC TRUMAN               | Comedy      |
| OPERATION OPERATION         | Comedy      |
| PARADISE SABRINA            | Comedy      |
| PARTY KNOCK                 | Comedy      |
| PERFECT GROOVE              | Comedy      |
| PINOCCHIO SIMON             | Comedy      |
| PURE RUNNER                 | Comedy      |
| RUSHMORE MERMAID            | Comedy      |
| SADDLE ANTITRUST            | Comedy      |
| SATURN NAME                 | Comedy      |
| SEARCHERS WAIT              | Comedy      |
| SNATCH SLIPPER              | Comedy      |
| STAGE WORLD                 | Comedy      |
| STRICTLY SCARFACE           | Comedy      |
| SUBMARINE BED               | Comedy      |
| SWEDEN SHINING              | Comedy      |
| TRAINSPOTTING STRANGERS     | Comedy      |
| TRAMP OTHERS                | Comedy      |
| VALLEY PACKER               | Comedy      |
| VELVET TERMINATOR           | Comedy      |
| VERTIGO NORTHWEST           | Comedy      |
| WISDOM WORKER               | Comedy      |
| ZORRO ARK                   | Comedy      |
| ACADEMY DINOSAUR            | Documentary |
| ADAPTATION HOLES            | Documentary |
| ARMY FLINTSTONES            | Documentary |
| BEACH HEARTBREAKERS         | Documentary |
| BED HIGHBALL                | Documentary |
| BILL OTHERS                 | Documentary |
| BONNIE HOLOCAUST            | Documentary |
| BROTHERHOOD BLANKET         | Documentary |
| CAUSE DATE                  | Documentary |
| CHICKEN HELLFIGHTERS        | Documentary |
| CIDER DESIRE                | Documentary |
| CLERKS ANGELS               | Documentary |
| COAST RAINBOW               | Documentary |
| CUPBOARD SINNERS            | Documentary |
| DANCING FEVER               | Documentary |
| DEEP CRUSADE                | Documentary |
| DELIVERANCE MULHOLLAND      | Documentary |
| DOZEN LION                  | Documentary |
| DUFFEL APOCALYPSE           | Documentary |
| EGG IGBY                    | Documentary |
| EXPENDABLE STALLION         | Documentary |
| FRENCH HOLIDAY              | Documentary |
| HALLOWEEN NUTS              | Documentary |
| HARDLY ROBBERS              | Documentary |
| HAWK CHILL                  | Documentary |
| HEAVYWEIGHTS BEAST          | Documentary |
| HOMEWARD CIDER              | Documentary |
| HUNTER ALTER                | Documentary |
| INDEPENDENCE HOTEL          | Documentary |
| INTOLERABLE INTENTIONS      | Documentary |
| KILL BROTHERHOOD            | Documentary |
| MADISON TRAP                | Documentary |
| MAJESTIC FLOATS             | Documentary |
| METAL ARMAGEDDON            | Documentary |
| MIDSUMMER GROUNDHOG         | Documentary |
| MIGHTY LUCK                 | Documentary |
| MOD SECRETARY               | Documentary |
| MODERN DORADO               | Documentary |
| NATIONAL STORY              | Documentary |
| NEWSIES STORY               | Documentary |
| NORTH TEQUILA               | Documentary |
| NOTORIOUS REUNION           | Documentary |
| PACIFIC AMISTAD             | Documentary |
| PELICAN COMFORTS            | Documentary |
| POCUS PULP                  | Documentary |
| PRINCESS GIANT              | Documentary |
| QUILLS BULL                 | Documentary |
| RAIDERS ANTITRUST           | Documentary |
| RAINBOW SHOCK               | Documentary |
| ROAD ROXANNE                | Documentary |
| SAGEBRUSH CLUELESS          | Documentary |
| SECRET GROUNDHOG            | Documentary |
| SHIP WONDERLAND             | Documentary |
| SHOW LORD                   | Documentary |
| SMOKING BARBARELLA          | Documentary |
| SPOILERS HELLFIGHTERS       | Documentary |
| STREAK RIDGEMONT            | Documentary |
| THIN SAGEBRUSH              | Documentary |
| UNITED PILOT                | Documentary |
| UNTOUCHABLES SUNRISE        | Documentary |
| VILLAIN DESPERATE           | Documentary |
| VIRGINIAN PLUTO             | Documentary |
| WAGON JAWS                  | Documentary |
| WARS PLUTO                  | Documentary |
| WEDDING APOLLO              | Documentary |
| WIFE TURN                   | Documentary |
| WRATH MILE                  | Documentary |
| YOUNG LANGUAGE              | Documentary |
| APOLLO TEEN                 | Drama       |
| BEAUTY GREASE               | Drama       |
| BEETHOVEN EXORCIST          | Drama       |
| BLADE POLISH                | Drama       |
| BRIGHT ENCOUNTERS           | Drama       |
| BUNCH MINDS                 | Drama       |
| CHILL LUCK                  | Drama       |
| CHITTY LOCK                 | Drama       |
| CONEHEADS SMOOCHY           | Drama       |
| CONFESSIONS MAGUIRE         | Drama       |
| CONQUERER NUTS              | Drama       |
| CRAFT OUTFIELD              | Drama       |
| DALMATIONS SWEDEN           | Drama       |
| DARKNESS WAR                | Drama       |
| DECEIVER BETRAYED           | Drama       |
| DESTINATION JERK            | Drama       |
| DIARY PANIC                 | Drama       |
| EDGE KISSING                | Drama       |
| ENCOUNTERS CURTAIN          | Drama       |
| GOLDFINGER SENSIBILITY      | Drama       |
| GONE TROUBLE                | Drama       |
| GREEDY ROOTS                | Drama       |
| HANGING DEEP                | Drama       |
| HAROLD FRENCH               | Drama       |
| HARRY IDAHO                 | Drama       |
| HOBBIT ALIEN                | Drama       |
| HUNCHBACK IMPOSSIBLE        | Drama       |
| JACKET FRISCO               | Drama       |
| KWAI HOMEWARD               | Drama       |
| LEBOWSKI SOLDIERS           | Drama       |
| LIES TREATMENT              | Drama       |
| LUCK OPUS                   | Drama       |
| MOB DUFFEL                  | Drama       |
| NECKLACE OUTBREAK           | Drama       |
| NOTTING SPEAKEASY           | Drama       |
| ORIENT CLOSER               | Drama       |
| PATHS CONTROL               | Drama       |
| PAYCHECK WAIT               | Drama       |
| PITY BOUND                  | Drama       |
| QUEEN LUKE                  | Drama       |
| RACER EGG                   | Drama       |
| REUNION WITCHES             | Drama       |
| ROCKY WAR                   | Drama       |
| SAINTS BRIDE                | Drama       |
| SAVANNAH TOWN               | Drama       |
| SCORPION APOLLO             | Drama       |
| SEA VIRGIN                  | Drama       |
| SEATTLE EXPECATIONS         | Drama       |
| SHOOTIST SUPERFLY           | Drama       |
| SLACKER LIAISONS            | Drama       |
| SOMETHING DUCK              | Drama       |
| SPICE SORORITY              | Drama       |
| TENENBAUMS COMMAND          | Drama       |
| TORQUE BOUND                | Drama       |
| TRANSLATION SUMMER          | Drama       |
| TREATMENT JEKYLL            | Drama       |
| UNFAITHFUL KILL             | Drama       |
| VIETNAM SMOOCHY             | Drama       |
| VIRGIN DAISY                | Drama       |
| WARDROBE PHANTOM            | Drama       |
| WEST LION                   | Drama       |
| WITCHES PANIC               | Drama       |
| AFRICAN EGG                 | Family      |
| APACHE DIVINE               | Family      |
| ATLANTIS CAUSE              | Family      |
| BAKED CLEOPATRA             | Family      |
| BANG KWAI                   | Family      |
| BEDAZZLED MARRIED           | Family      |
| BILKO ANONYMOUS             | Family      |
| BLANKET BEVERLY             | Family      |
| BLOOD ARGONAUTS             | Family      |
| BLUES INSTINCT              | Family      |
| BRAVEHEART HUMAN            | Family      |
| CHASING FIGHT               | Family      |
| CHISUM BEHAVIOR             | Family      |
| CHOCOLAT HARRY              | Family      |
| CONFUSED CANDLES            | Family      |
| CONVERSATION DOWNHILL       | Family      |
| DATE SPEED                  | Family      |
| DINOSAUR SECRETARY          | Family      |
| DUMBO LUST                  | Family      |
| EARRING INSTINCT            | Family      |
| EFFECT GLADIATOR            | Family      |
| FEUD FROGMEN                | Family      |
| FINDING ANACONDA            | Family      |
| GABLES METROPOLIS           | Family      |
| GANDHI KWAI                 | Family      |
| GLADIATOR WESTWARD          | Family      |
| GREASE YOUTH                | Family      |
| HALF OUTFIELD               | Family      |
| HOCUS FRIDA                 | Family      |
| HOMICIDE PEACH              | Family      |
| HOUSE DYNAMITE              | Family      |
| HUNTING MUSKETEERS          | Family      |
| INDIAN LOVE                 | Family      |
| JASON TRAP                  | Family      |
| JEDI BENEATH                | Family      |
| KILLER INNOCENT             | Family      |
| KING EVOLUTION              | Family      |
| LOLITA WORLD                | Family      |
| LOUISIANA HARRY             | Family      |
| MAGUIRE APACHE              | Family      |
| MANCHURIAN CURTAIN          | Family      |
| MOVIE SHAKESPEARE           | Family      |
| MUSIC BOONDOCK              | Family      |
| NATURAL STOCK               | Family      |
| NETWORK PEAK                | Family      |
| ODDS BOOGIE                 | Family      |
| OPPOSITE NECKLACE           | Family      |
| PILOT HOOSIERS              | Family      |
| PITTSBURGH HUNCHBACK        | Family      |
| PRESIDENT BANG              | Family      |
| PRIX UNDEFEATED             | Family      |
| RAGE GAMES                  | Family      |
| RANGE MOONWALKER            | Family      |
| REMEMBER DIARY              | Family      |
| RESURRECTION SILVERADO      | Family      |
| ROBBERY BRIGHT              | Family      |
| RUSH GOODFELLAS             | Family      |
| SECRETS PARADISE            | Family      |
| SENSIBILITY REAR            | Family      |
| SIEGE MADRE                 | Family      |
| SLUMS DUCK                  | Family      |
| SOUP WISDOM                 | Family      |
| SPARTACUS CHEAPER           | Family      |
| SPINAL ROCKY                | Family      |
| SPLASH GUMP                 | Family      |
| SUNSET RACER                | Family      |
| SUPER WYOMING               | Family      |
| VIRTUAL SPOILERS            | Family      |
| WILLOW TRACY                | Family      |
| AGENT TRUMAN                | Foreign     |
| ALAMO VIDEOTAPE             | Foreign     |
| ALIEN CENTER                | Foreign     |
| ALLEY EVOLUTION             | Foreign     |
| BABY HALL                   | Foreign     |
| BALLROOM MOCKINGBIRD        | Foreign     |
| BROOKLYN DESERT             | Foreign     |
| BUGSY SONG                  | Foreign     |
| CALENDAR GUNFIGHT           | Foreign     |
| CATCH AMISTAD               | Foreign     |
| CHOCOLATE DUCK              | Foreign     |
| COMMAND DARLING             | Foreign     |
| COWBOY DOOM                 | Foreign     |
| CROSSING DIVORCE            | Foreign     |
| CRYSTAL BREAKING            | Foreign     |
| CYCLONE FAMILY              | Foreign     |
| DANGEROUS UPTOWN            | Foreign     |
| DOUBTFIRE LABYRINTH         | Foreign     |
| EVERYONE CRAFT              | Foreign     |
| FICTION CHRISTMAS           | Foreign     |
| FRIDA SLIPPER               | Foreign     |
| GENTLEMEN STAGE             | Foreign     |
| GRAPES FURY                 | Foreign     |
| GREEK EVERYONE              | Foreign     |
| HAPPINESS UNITED            | Foreign     |
| HELLFIGHTERS SIERRA         | Foreign     |
| HIGHBALL POTTER             | Foreign     |
| HOLIDAY GAMES               | Foreign     |
| HOOSIERS BIRDCAGE           | Foreign     |
| HOTEL HAPPINESS             | Foreign     |
| HUNGER ROOF                 | Foreign     |
| ILLUSION AMELIE             | Foreign     |
| IMPOSSIBLE PREJUDICE        | Foreign     |
| INFORMER DOUBLE             | Foreign     |
| INNOCENT USUAL              | Foreign     |
| INTRIGUE WORST              | Foreign     |
| JET NEIGHBORS               | Foreign     |
| KANE EXORCIST               | Foreign     |
| KISS GLORY                  | Foreign     |
| LOSE INCH                   | Foreign     |
| LOST BIRD                   | Foreign     |
| MADNESS ATTACKS             | Foreign     |
| MATRIX SNOWMAN              | Foreign     |
| MAUDE MOD                   | Foreign     |
| MEET CHOCOLATE              | Foreign     |
| MIXED DOORS                 | Foreign     |
| MOON BUNCH                  | Foreign     |
| MULHOLLAND BEAST            | Foreign     |
| MUPPET MILE                 | Foreign     |
| NEWTON LABYRINTH            | Foreign     |
| OPUS ICE                    | Foreign     |
| ORANGE GRAPES               | Foreign     |
| PAST SUICIDES               | Foreign     |
| PEARL DESTINY               | Foreign     |
| PET HAUNTING                | Foreign     |
| POLLOCK DELIVERANCE         | Foreign     |
| PURPLE MOVIE                | Foreign     |
| RESERVOIR ADAPTATION        | Foreign     |
| ROCKETEER MOTHER            | Foreign     |
| SCHOOL JACKET               | Foreign     |
| SCISSORHANDS SLUMS          | Foreign     |
| SHOCK CABIN                 | Foreign     |
| SHREK LICENSE               | Foreign     |
| SORORITY QUEEN              | Foreign     |
| STEPMOM DREAM               | Foreign     |
| TOWN ARK                    | Foreign     |
| TRAP GUYS                   | Foreign     |
| USUAL UNTOUCHABLES          | Foreign     |
| VISION TORQUE               | Foreign     |
| WAR NOTTING                 | Foreign     |
| WASH HEAVENLY               | Foreign     |
| WHALE BIKINI                | Foreign     |
| WONDERFUL DROP              | Foreign     |
| AUTUMN CROW                 | Games       |
| BULWORTH COMMANDMENTS       | Games       |
| CANDLES GRAPES              | Games       |
| CHICAGO NORTH               | Games       |
| CREATURES SHAKESPEARE       | Games       |
| CURTAIN VIDEOTAPE           | Games       |
| DARLING BREAKING            | Games       |
| DAWN POND                   | Games       |
| DAZED PUNK                  | Games       |
| DETAILS PACKER              | Games       |
| DIRTY ACE                   | Games       |
| DIVINE RESURRECTION         | Games       |
| DWARFS ALTER                | Games       |
| ENCINO ELF                  | Games       |
| FANTASIA PARK               | Games       |
| FEATHERS METAL              | Games       |
| FEVER EMPIRE                | Games       |
| FIRE WOLVES                 | Games       |
| FORWARD TEMPLE              | Games       |
| GATHERING CALENDAR          | Games       |
| GLORY TRACY                 | Games       |
| GRINCH MASSAGE              | Games       |
| GRIT CLOCKWORK              | Games       |
| GUN BONNIE                  | Games       |
| HAUNTING PIANIST            | Games       |
| HEAD STRANGER               | Games       |
| HUMAN GRAFFITI              | Games       |
| ICE CROSSING                | Games       |
| JERICHO MULAN               | Games       |
| LADYBUGS ARMAGEDDON         | Games       |
| LAMBS CINCINATTI            | Games       |
| MADRE GABLES                | Games       |
| MALTESE HOPE                | Games       |
| MARS ROMAN                  | Games       |
| MASSACRE USUAL              | Games       |
| MONSOON CAUSE               | Games       |
| MOONSHINE CABIN             | Games       |
| MOONWALKER FOOL             | Games       |
| NAME DETECTIVE              | Games       |
| NIGHTMARE CHILL             | Games       |
| OUTBREAK DIVINE             | Games       |
| PANKY SUBMARINE             | Games       |
| PIZZA JUMANJI               | Games       |
| PRIVATE DROP                | Games       |
| PSYCHO SHRUNK               | Games       |
| ROOF CHAMPION               | Games       |
| ROUGE SQUAD                 | Games       |
| ROXANNE REBEL               | Games       |
| SASSY PACKER                | Games       |
| SEVEN SWARM                 | Games       |
| SLEUTH ORIENT               | Games       |
| SPY MILE                    | Games       |
| STAMPEDE DISTURBING         | Games       |
| STATE WASTELAND             | Games       |
| SUIT WALLS                  | Games       |
| TYCOON GATHERING            | Games       |
| VANILLA DAY                 | Games       |
| VIDEOTAPE ARSENIC           | Games       |
| VOLCANO TEXAS               | Games       |
| WANDA CHAMBER               | Games       |
| WIND PHANTOM                | Games       |
| ACE GOLDFINGER              | Horror      |
| AFFAIR PREJUDICE            | Horror      |
| AIRPORT POLLOCK             | Horror      |
| ALABAMA DEVIL               | Horror      |
| ALI FOREVER                 | Horror      |
| ANALYZE HOOSIERS            | Horror      |
| ANYTHING SAVANNAH           | Horror      |
| ARABIA DOGMA                | Horror      |
| ARACHNOPHOBIA ROLLERCOASTER | Horror      |
| BEHAVIOR RUNAWAY            | Horror      |
| BOWFINGER GABLES            | Horror      |
| CARRIE BUNCH                | Horror      |
| COMMANDMENTS EXPRESS        | Horror      |
| DESERT POSEIDON             | Horror      |
| DRUMS DYNAMITE              | Horror      |
| EGYPT TENENBAUMS            | Horror      |
| ELEPHANT TROJAN             | Horror      |
| FAMILY SWEET                | Horror      |
| FIDELITY DEVIL              | Horror      |
| FREDDY STORM                | Horror      |
| GASLIGHT CRUSADE            | Horror      |
| HIGH ENCINO                 | Horror      |
| JAPANESE RUN                | Horror      |
| KARATE MOON                 | Horror      |
| KENTUCKIAN GIANT            | Horror      |
| LADY STAGE                  | Horror      |
| LOLA AGENT                  | Horror      |
| LOVE SUICIDES               | Horror      |
| MONTEREY LABYRINTH          | Horror      |
| MOTIONS DETAILS             | Horror      |
| PANIC CLUB                  | Horror      |
| PARIS WEEKEND               | Horror      |
| PATTON INTERVIEW            | Horror      |
| PULP BEVERLY                | Horror      |
| REAP UNFAITHFUL             | Horror      |
| REEF SALUTE                 | Horror      |
| ROCK INSTINCT               | Horror      |
| ROLLERCOASTER BRINGING      | Horror      |
| RULES HUMAN                 | Horror      |
| SIMON NORTH                 | Horror      |
| SINNERS ATLANTIS            | Horror      |
| SLEEPING SUSPECTS           | Horror      |
| SPIRIT FLINTSTONES          | Horror      |
| STRANGERS GRAFFITI          | Horror      |
| STREETCAR INTENTIONS        | Horror      |
| SWARM GOLD                  | Horror      |
| TARZAN VIDEOTAPE            | Horror      |
| TEMPLE ATTRACTION           | Horror      |
| TEXAS WATCH                 | Horror      |
| TRAIN BUNCH                 | Horror      |
| TREASURE COMMAND            | Horror      |
| UNDEFEATED DALMATIONS       | Horror      |
| WATERSHIP FRONTIER          | Horror      |
| WORLD LEATHERNECKS          | Horror      |
| YENTL IDAHO                 | Horror      |
| ZHIVAGO CORE                | Horror      |
| ALASKA PHANTOM              | Music       |
| ALONE TRIP                  | Music       |
| AMELIE HELLFIGHTERS         | Music       |
| BALLOON HOMEWARD            | Music       |
| BANGER PINOCCHIO            | Music       |
| BIRCH ANTITRUST             | Music       |
| BIRDCAGE CASPER             | Music       |
| BOOGIE AMELIE               | Music       |
| CHAMBER ITALIAN             | Music       |
| CLONES PINOCCHIO            | Music       |
| CLUE GRAIL                  | Music       |
| CONFIDENTIAL INTERVIEW      | Music       |
| DEER VIRGINIAN              | Music       |
| DORADO NOTTING              | Music       |
| DRIVING POLISH              | Music       |
| ELF MURDER                  | Music       |
| ENEMY ODDS                  | Music       |
| FREAKY POCUS                | Music       |
| GO PURPLE                   | Music       |
| GREATEST NORTH              | Music       |
| GROSSE WONDERFUL            | Music       |
| HANOVER GALAXY              | Music       |
| HEAVENLY GUN                | Music       |
| HOME PITY                   | Music       |
| IMPACT ALADDIN              | Music       |
| INSIDER ARIZONA             | Music       |
| JAWBREAKER BROOKLYN         | Music       |
| LEGEND JEDI                 | Music       |
| LUCKY FLYING                | Music       |
| MASKED BUBBLE               | Music       |
| MINORITY KISS               | Music       |
| MONSTER SPARTACUS           | Music       |
| OLEANDER CLUE               | Music       |
| OUTFIELD MASSACRE           | Music       |
| PERSONAL LADYBUGS           | Music       |
| REBEL AIRPORT               | Music       |
| REDS POCUS                  | Music       |
| ROMAN PUNK                  | Music       |
| RUNNER MADIGAN              | Music       |
| SCALAWAG DUCK               | Music       |
| SILENCE KANE                | Music       |
| SONG HEDWIG                 | Music       |
| TAXI KICK                   | Music       |
| TELEGRAPH VOYAGE            | Music       |
| TERMINATOR CLUB             | Music       |
| UNCUT SUICIDES              | Music       |
| VANISHING ROCKY             | Music       |
| WIZARD COLDBLOODED          | Music       |
| WON DARES                   | Music       |
| WORDS HUNTER                | Music       |
| YOUTH KICK                  | Music       |
| AMISTAD MIDSUMMER           | New         |
| ANGELS LIFE                 | New         |
| APOCALYPSE FLAMINGOS        | New         |
| ATTRACTION NEWTON           | New         |
| BIRDS PERDITION             | New         |
| BOULEVARD MOB               | New         |
| BRANNIGAN SUNRISE           | New         |
| BREAKFAST GOLDFINGER        | New         |
| BREAKING HOME               | New         |
| BUTCH PANTHER               | New         |
| BUTTERFLY CHOCOLAT          | New         |
| CHAPLIN LICENSE             | New         |
| CHINATOWN GLADIATOR         | New         |
| CLEOPATRA DEVIL             | New         |
| CLYDE THEORY                | New         |
| DAY UNFAITHFUL              | New         |
| DESTINY SATURDAY            | New         |
| DRAGONFLY STRANGERS         | New         |
| EAGLES PANKY                | New         |
| EARTH VISION                | New         |
| ENDING CROWDS               | New         |
| EVE RESURRECTION            | New         |
| FATAL HAUNTED               | New         |
| FLAMINGOS CONNECTICUT       | New         |
| FLASH WARS                  | New         |
| FRONTIER CABIN              | New         |
| GODFATHER DIARY             | New         |
| HOURS RAGE                  | New         |
| IDAHO LOVE                  | New         |
| INTERVIEW LIAISONS          | New         |
| JEKYLL FROGMEN              | New         |
| JUMANJI BLADE               | New         |
| JUNGLE CLOSER               | New         |
| LOVERBOY ATTACKS            | New         |
| MAIDEN HOME                 | New         |
| MANNEQUIN WORST             | New         |
| MASK PEACH                  | New         |
| MINE TITANS                 | New         |
| MONEY HAROLD                | New         |
| NUTS TIES                   | New         |
| OKLAHOMA JUMANJI            | New         |
| PHANTOM GLORY               | New         |
| PIANIST OUTFIELD            | New         |
| PLATOON INSTINCT            | New         |
| PLUTO OLEANDER              | New         |
| REDEMPTION COMFORTS         | New         |
| RIDGEMONT SUBMARINE         | New         |
| RUN PACIFIC                 | New         |
| RUNAWAY TENENBAUMS          | New         |
| SALUTE APOLLO               | New         |
| SAMURAI LION                | New         |
| SLEEPY JAPANESE             | New         |
| STING PERSONAL              | New         |
| STOCK GLASS                 | New         |
| TROOPERS METAL              | New         |
| UNBREAKABLE KARATE          | New         |
| VAMPIRE WHALE               | New         |
| VANISHED GARDEN             | New         |
| VARSITY TRIP                | New         |
| VOICE PEACH                 | New         |
| WAKE JAWS                   | New         |
| WILD APOLLO                 | New         |
| WYOMING STORM               | New         |
| ANNIE IDENTITY              | Sci-Fi      |
| ARMAGEDDON LOST             | Sci-Fi      |
| ATTACKS HATE                | Sci-Fi      |
| BADMAN DAWN                 | Sci-Fi      |
| BARBARELLA STREETCAR        | Sci-Fi      |
| BEVERLY OUTLAW              | Sci-Fi      |
| BINGO TALENTED              | Sci-Fi      |
| BLINDNESS GUN               | Sci-Fi      |
| CAMELOT VACATION            | Sci-Fi      |
| CHAINSAW UPTOWN             | Sci-Fi      |
| CHARADE DUFFEL              | Sci-Fi      |
| CHARIOTS CONSPIRACY         | Sci-Fi      |
| CHEAPER CLYDE               | Sci-Fi      |
| CINCINATTI WHISPERER        | Sci-Fi      |
| CITIZEN SHREK               | Sci-Fi      |
| COLDBLOODED DARLING         | Sci-Fi      |
| CONNECTICUT TRAMP           | Sci-Fi      |
| CROWDS TELEMARK             | Sci-Fi      |
| DAISY MENAGERIE             | Sci-Fi      |
| DISTURBING SCARFACE         | Sci-Fi      |
| DIVIDE MONSTER              | Sci-Fi      |
| DOLLS RAGE                  | Sci-Fi      |
| ENGLISH BULWORTH            | Sci-Fi      |
| EXPRESS LONELY              | Sci-Fi      |
| EYES DRIVING                | Sci-Fi      |
| FIDDLER LOST                | Sci-Fi      |
| FISH OPUS                   | Sci-Fi      |
| FRISCO FORREST              | Sci-Fi      |
| GARDEN ISLAND               | Sci-Fi      |
| GOLDMINE TYCOON             | Sci-Fi      |
| GOODFELLAS SALUTE           | Sci-Fi      |
| GRAFFITI LOVE               | Sci-Fi      |
| GUYS FALCON                 | Sci-Fi      |
| HAMLET WISDOM               | Sci-Fi      |
| HANKY OCTOBER               | Sci-Fi      |
| HOLLOW JEOPARDY             | Sci-Fi      |
| IDENTITY LOVER              | Sci-Fi      |
| LICENSE WEEKEND             | Sci-Fi      |
| MARRIED GO                  | Sci-Fi      |
| METROPOLIS COMA             | Sci-Fi      |
| MOURNING PURPLE             | Sci-Fi      |
| NEMO CAMPUS                 | Sci-Fi      |
| NONE SPIKING                | Sci-Fi      |
| OPEN AFRICAN                | Sci-Fi      |
| PANTHER REDS                | Sci-Fi      |
| RAGING AIRPLANE             | Sci-Fi      |
| RANDOM GO                   | Sci-Fi      |
| REIGN GENTLEMEN             | Sci-Fi      |
| SILVERADO GOLDFINGER        | Sci-Fi      |
| SOLDIERS EVOLUTION          | Sci-Fi      |
| SPIRITED CASUALTIES         | Sci-Fi      |
| STALLION SUNDANCE           | Sci-Fi      |
| SUICIDES SILENCE            | Sci-Fi      |
| SUN CONFESSIONS             | Sci-Fi      |
| TITANS JERK                 | Sci-Fi      |
| TROJAN TOMORROW             | Sci-Fi      |
| UNFORGIVEN ZOOLANDER        | Sci-Fi      |
| VACATION BOONDOCK           | Sci-Fi      |
| WEEKEND PERSONAL            | Sci-Fi      |
| WHISPERER GIANT             | Sci-Fi      |
| WONDERLAND CHRISTMAS        | Sci-Fi      |
| ALADDIN CALENDAR            | Sports      |
| ANONYMOUS HUMAN             | Sports      |
| ARTIST COLDBLOODED          | Sports      |
| BUBBLE GROSSE               | Sports      |
| CALIFORNIA BIRDS            | Sports      |
| CARIBBEAN LIBERTY           | Sports      |
| CHANCE RESURRECTION         | Sports      |
| CONGENIALITY QUEST          | Sports      |
| CRANES RESERVOIR            | Sports      |
| CRUSADE HONEY               | Sports      |
| DIVORCE SHINING             | Sports      |
| DRIVER ANNIE                | Sports      |
| DROP WATERFRONT             | Sports      |
| DUDE BLINDNESS              | Sports      |
| DURHAM PANKY                | Sports      |
| ELIZABETH SHANE             | Sports      |
| EVOLUTION ALTER             | Sports      |
| EXORCIST STING              | Sports      |
| FLATLINERS KILLER           | Sports      |
| FLIGHT LIES                 | Sports      |
| GLEAMING JAWBREAKER         | Sports      |
| GRACELAND DYNAMITE          | Sports      |
| GROOVE FICTION              | Sports      |
| GUNFIGHTER MUSSOLINI        | Sports      |
| HOLES BRANNIGAN             | Sports      |
| HONEY TIES                  | Sports      |
| HYSTERICAL GRAIL            | Sports      |
| IMAGE PRINCESS              | Sports      |
| INSTINCT AIRPORT            | Sports      |
| JADE BUNCH                  | Sports      |
| JOON NORTHWEST              | Sports      |
| KRAMER CHOCOLATE            | Sports      |
| LESSON CLEOPATRA            | Sports      |
| LIBERTY MAGNIFICENT         | Sports      |
| LOSER HUSTLER               | Sports      |
| MERMAID INSECTS             | Sports      |
| MILE MULAN                  | Sports      |
| MOSQUITO ARMAGEDDON         | Sports      |
| MOTHER OLEANDER             | Sports      |
| MUMMY CREATURES             | Sports      |
| MUSSOLINI SPOILERS          | Sports      |
| NEIGHBORS CHARADE           | Sports      |
| NORTHWEST POLISH            | Sports      |
| NOVOCAINE FLIGHT            | Sports      |
| PEACH INNOCENT              | Sports      |
| PEAK FOREVER                | Sports      |
| PERDITION FARGO             | Sports      |
| PHILADELPHIA WIFE           | Sports      |
| PICKUP DRIVING              | Sports      |
| PIRATES ROXANNE             | Sports      |
| POSEIDON FOREVER            | Sports      |
| RECORDS ZORRO               | Sports      |
| RIDER CADDYSHACK            | Sports      |
| RIVER OUTLAW                | Sports      |
| ROSES TREASURE              | Sports      |
| SATISFACTION CONFIDENTIAL   | Sports      |
| SATURDAY LAMBS              | Sports      |
| SEABISCUIT PUNK             | Sports      |
| SECRETARY ROUGE             | Sports      |
| SENSE GREEK                 | Sports      |
| SHAKESPEARE SADDLE          | Sports      |
| SIERRA DIVIDE               | Sports      |
| SLIPPER FIDELITY            | Sports      |
| SMOOCHY CONTROL             | Sports      |
| SQUAD FISH                  | Sports      |
| STAR OPERATION              | Sports      |
| STEERS ARMAGEDDON           | Sports      |
| STRAIGHT HOURS              | Sports      |
| TALENTED HOMICIDE           | Sports      |
| TIGHTS DAWN                 | Sports      |
| TOURIST PELICAN             | Sports      |
| TRADING PINOCCHIO           | Sports      |
| TUXEDO MILE                 | Sports      |
| VICTORY ACADEMY             | Sports      |
| ARSENIC INDEPENDENCE        | Travel      |
| BASIC EASY                  | Travel      |
| BIRD INDEPENDENCE           | Travel      |
| BOILED DARES                | Travel      |
| BOONDOCK BALLROOM           | Travel      |
| BORN SPINAL                 | Travel      |
| BUCKET BROTHERHOOD          | Travel      |
| CASABLANCA SUPER            | Travel      |
| CASSIDY WYOMING             | Travel      |
| COMA HEAD                   | Travel      |
| COMFORTS RUSH               | Travel      |
| CONTACT ANONYMOUS           | Travel      |
| DESPERATE TRAINSPOTTING     | Travel      |
| DISCIPLE MOTHER             | Travel      |
| DRUMLINE CYCLONE            | Travel      |
| ENOUGH RAGING               | Travel      |
| ESCAPE METROPOLIS           | Travel      |
| EXPECATIONS NATURAL         | Travel      |
| FACTORY DRAGON              | Travel      |
| FELLOWSHIP AUTUMN           | Travel      |
| FROGMEN BREAKING            | Travel      |
| FUGITIVE MAGUIRE            | Travel      |
| GAMES BOWFINGER             | Travel      |
| GUMP DATE                   | Travel      |
| HAUNTED ANTITRUST           | Travel      |
| HORROR REIGN                | Travel      |
| IGBY MAKER                  | Travel      |
| ITALIAN AFRICAN             | Travel      |
| KICK SAVANNAH               | Travel      |
| LEATHERNECKS DWARFS         | Travel      |
| LIAISONS SWEET              | Travel      |
| LOCK REAR                   | Travel      |
| MADIGAN DORADO              | Travel      |
| MOULIN WAKE                 | Travel      |
| MUSCLE BRIGHT               | Travel      |
| ORDER BETRAYED              | Travel      |
| OTHERS SOUP                 | Travel      |
| OUTLAW HANKY                | Travel      |
| PAPI NECKLACE               | Travel      |
| SHANE DARKNESS              | Travel      |
| SHANGHAI TYCOON             | Travel      |
| SHAWSHANK BUBBLE            | Travel      |
| SHINING ROSES               | Travel      |
| SMILE EARRING               | Travel      |
| SPEED SUIT                  | Travel      |
| STONE FIRE                  | Travel      |
| SUPERFLY TRIP               | Travel      |
| SWEET BROTHERHOOD           | Travel      |
| TEEN APOLLO                 | Travel      |
| TOMATOES HELLFIGHTERS       | Travel      |
| TRAFFIC HOBBIT              | Travel      |
| TROUBLE DATE                | Travel      |
| VALENTINE VANISHING         | Travel      |
| WINDOW SIDE                 | Travel      |
| WOLVES DESIRE               | Travel      |
| WORKER TARZAN               | Travel      |
| WORKING MICROCOSMOS         | Travel      |
+-----------------------------+-------------+
1000 rows in set (0,00 sec)
   ```

4. Listar los nombres de las ciudades junto con sus países.

```mysql
SELECT c.nombre, p.nombre
FROM ciudad as c 
INNER JOIN pais as p ON p.id_pais = c.id_pais; 

+----------------------------+---------------------------------------+
| nombre                     | nombre                                |
+----------------------------+---------------------------------------+
| Kabul                      | Afghanistan                           |
| Batna                      | Algeria                               |
| Bchar                      | Algeria                               |
| Skikda                     | Algeria                               |
| Tafuna                     | American Samoa                        |
| Benguela                   | Angola                                |
| Namibe                     | Angola                                |
| South Hill                 | Anguilla                              |
| Almirante Brown            | Argentina                             |
| Avellaneda                 | Argentina                             |
| Baha Blanca                | Argentina                             |
| Crdoba                     | Argentina                             |
| Escobar                    | Argentina                             |
| Ezeiza                     | Argentina                             |
| La Plata                   | Argentina                             |
| Merlo                      | Argentina                             |
| Quilmes                    | Argentina                             |
| San Miguel de Tucumn       | Argentina                             |
| Santa F                    | Argentina                             |
| Tandil                     | Argentina                             |
| Vicente Lpez               | Argentina                             |
| Yerevan                    | Armenia                               |
| Woodridge                  | Australia                             |
| Graz                       | Austria                               |
| Linz                       | Austria                               |
| Salzburg                   | Austria                               |
| Baku                       | Azerbaijan                            |
| Sumqayit                   | Azerbaijan                            |
| al-Manama                  | Bahrain                               |
| Dhaka                      | Bangladesh                            |
| Jamalpur                   | Bangladesh                            |
| Tangail                    | Bangladesh                            |
| Mogiljov                   | Belarus                               |
| Molodetno                  | Belarus                               |
| El Alto                    | Bolivia                               |
| Sucre                      | Bolivia                               |
| Alvorada                   | Brazil                                |
| Angra dos Reis             | Brazil                                |
| Anpolis                    | Brazil                                |
| Aparecida de Goinia        | Brazil                                |
| Araatuba                   | Brazil                                |
| Bag                        | Brazil                                |
| Belm                       | Brazil                                |
| Blumenau                   | Brazil                                |
| Boa Vista                  | Brazil                                |
| Braslia                    | Brazil                                |
| Goinia                     | Brazil                                |
| Guaruj                     | Brazil                                |
| guas Lindas de Gois        | Brazil                                |
| Ibirit                     | Brazil                                |
| Juazeiro do Norte          | Brazil                                |
| Juiz de Fora               | Brazil                                |
| Luzinia                    | Brazil                                |
| Maring                     | Brazil                                |
| Po                         | Brazil                                |
| Poos de Caldas             | Brazil                                |
| Rio Claro                  | Brazil                                |
| Santa Brbara dOeste        | Brazil                                |
| Santo Andr                 | Brazil                                |
| So Bernardo do Campo       | Brazil                                |
| So Leopoldo                | Brazil                                |
| Sorocaba                   | Brazil                                |
| Vila Velha                 | Brazil                                |
| Vitria de Santo Anto       | Brazil                                |
| Bandar Seri Begawan        | Brunei                                |
| Ruse                       | Bulgaria                              |
| Stara Zagora               | Bulgaria                              |
| Battambang                 | Cambodia                              |
| Phnom Penh                 | Cambodia                              |
| Bamenda                    | Cameroon                              |
| Yaound                     | Cameroon                              |
| Gatineau                   | Canada                                |
| Halifax                    | Canada                                |
| Lethbridge                 | Canada                                |
| London                     | Canada                                |
| Oshawa                     | Canada                                |
| Richmond Hill              | Canada                                |
| Vancouver                  | Canada                                |
| NDjamna                    | Chad                                  |
| Antofagasta                | Chile                                 |
| Coquimbo                   | Chile                                 |
| Rancagua                   | Chile                                 |
| Baicheng                   | China                                 |
| Baiyin                     | China                                 |
| Binzhou                    | China                                 |
| Changzhou                  | China                                 |
| Datong                     | China                                 |
| Daxian                     | China                                 |
| Dongying                   | China                                 |
| Emeishan                   | China                                 |
| Enshi                      | China                                 |
| Ezhou                      | China                                 |
| Fuyu                       | China                                 |
| Fuzhou                     | China                                 |
| Haining                    | China                                 |
| Hami                       | China                                 |
| Hohhot                     | China                                 |
| Huaian                     | China                                 |
| Jinchang                   | China                                 |
| Jining                     | China                                 |
| Jinzhou                    | China                                 |
| Junan                      | China                                 |
| Korla                      | China                                 |
| Laiwu                      | China                                 |
| Laohekou                   | China                                 |
| Lengshuijiang              | China                                 |
| Leshan                     | China                                 |
| Liaocheng                  | China                                 |
| Meixian                    | China                                 |
| Nanyang                    | China                                 |
| Pingxiang                  | China                                 |
| Qinhuangdao                | China                                 |
| Rizhao                     | China                                 |
| Sanya                      | China                                 |
| Shanwei                    | China                                 |
| Shaoguan                   | China                                 |
| Shenzhen                   | China                                 |
| Suihua                     | China                                 |
| Tianjin                    | China                                 |
| Tiefa                      | China                                 |
| Tieli                      | China                                 |
| Tongliao                   | China                                 |
| Weifang                    | China                                 |
| Xiangfan                   | China                                 |
| Xiangtan                   | China                                 |
| Xintai                     | China                                 |
| Xinxiang                   | China                                 |
| Yantai                     | China                                 |
| Yinchuan                   | China                                 |
| Yingkou                    | China                                 |
| Yuncheng                   | China                                 |
| Yuzhou                     | China                                 |
| Zalantun                   | China                                 |
| Zaoyang                    | China                                 |
| Zhoushan                   | China                                 |
| Buenaventura               | Colombia                              |
| Dos Quebradas              | Colombia                              |
| Florencia                  | Colombia                              |
| Pereira                    | Colombia                              |
| Sincelejo                  | Colombia                              |
| Sogamoso                   | Colombia                              |
| Lubumbashi                 | Congo, The Democratic Republic of the |
| Mwene-Ditu                 | Congo, The Democratic Republic of the |
| Olomouc                    | Czech Republic                        |
| La Romana                  | Dominican Republic                    |
| San Felipe de Puerto Plata | Dominican Republic                    |
| Santiago de los Caballeros | Dominican Republic                    |
| Loja                       | Ecuador                               |
| Portoviejo                 | Ecuador                               |
| Robamba                    | Ecuador                               |
| Bilbays                    | Egypt                                 |
| Idfu                       | Egypt                                 |
| Mit Ghamr                  | Egypt                                 |
| Qalyub                     | Egypt                                 |
| Sawhaj                     | Egypt                                 |
| Shubra al-Khayma           | Egypt                                 |
| Tartu                      | Estonia                               |
| Addis Abeba                | Ethiopia                              |
| Trshavn                    | Faroe Islands                         |
| Oulu                       | Finland                               |
| Brest                      | France                                |
| Le Mans                    | France                                |
| Toulon                     | France                                |
| Toulouse                   | France                                |
| Cayenne                    | French Guiana                         |
| Faaa                       | French Polynesia                      |
| Papeete                    | French Polynesia                      |
| Banjul                     | Gambia                                |
| Duisburg                   | Germany                               |
| Erlangen                   | Germany                               |
| Halle/Saale                | Germany                               |
| Mannheim                   | Germany                               |
| Saarbrcken                 | Germany                               |
| Siegen                     | Germany                               |
| Witten                     | Germany                               |
| Athenai                    | Greece                                |
| Patras                     | Greece                                |
| Nuuk                       | Greenland                             |
| Citt del Vaticano          | Holy See (Vatican City State)         |
| Kowloon and New Kowloon    | Hong Kong                             |
| Szkesfehrvr                | Hungary                               |
| Adoni                      | India                                 |
| Ahmadnagar                 | India                                 |
| Allappuzha (Alleppey)      | India                                 |
| Ambattur                   | India                                 |
| Amroha                     | India                                 |
| Balurghat                  | India                                 |
| Berhampore (Baharampur)    | India                                 |
| Bhavnagar                  | India                                 |
| Bhilwara                   | India                                 |
| Bhimavaram                 | India                                 |
| Bhopal                     | India                                 |
| Bhusawal                   | India                                 |
| Bijapur                    | India                                 |
| Chandrapur                 | India                                 |
| Chapra                     | India                                 |
| Dhule (Dhulia)             | India                                 |
| Etawah                     | India                                 |
| Firozabad                  | India                                 |
| Gandhinagar                | India                                 |
| Gulbarga                   | India                                 |
| Haldia                     | India                                 |
| Halisahar                  | India                                 |
| Hoshiarpur                 | India                                 |
| Hubli-Dharwad              | India                                 |
| Jaipur                     | India                                 |
| Jhansi                     | India                                 |
| Jodhpur                    | India                                 |
| Kamarhati                  | India                                 |
| Kanchrapara                | India                                 |
| Karnal                     | India                                 |
| Katihar                    | India                                 |
| Kumbakonam                 | India                                 |
| Miraj                      | India                                 |
| Munger (Monghyr)           | India                                 |
| Mysore                     | India                                 |
| Nagaon                     | India                                 |
| Palghat (Palakkad)         | India                                 |
| Parbhani                   | India                                 |
| Pathankot                  | India                                 |
| Patiala                    | India                                 |
| Pudukkottai                | India                                 |
| Pune                       | India                                 |
| Purnea (Purnia)            | India                                 |
| Rae Bareli                 | India                                 |
| Rajkot                     | India                                 |
| Rampur                     | India                                 |
| Ranchi                     | India                                 |
| Sambhal                    | India                                 |
| Satna                      | India                                 |
| Shimoga                    | India                                 |
| Shivapuri                  | India                                 |
| Siliguri (Shiliguri)       | India                                 |
| Tambaram                   | India                                 |
| Udaipur                    | India                                 |
| Uluberia                   | India                                 |
| Uttarpara-Kotrung          | India                                 |
| Valparai                   | India                                 |
| Varanasi (Benares)         | India                                 |
| Vijayawada                 | India                                 |
| Yamuna Nagar               | India                                 |
| Cianjur                    | Indonesia                             |
| Ciomas                     | Indonesia                             |
| Ciparay                    | Indonesia                             |
| Gorontalo                  | Indonesia                             |
| Jakarta                    | Indonesia                             |
| Lhokseumawe                | Indonesia                             |
| Madiun                     | Indonesia                             |
| Pangkal Pinang             | Indonesia                             |
| Pemalang                   | Indonesia                             |
| Pontianak                  | Indonesia                             |
| Probolinggo                | Indonesia                             |
| Purwakarta                 | Indonesia                             |
| Surakarta                  | Indonesia                             |
| Tegal                      | Indonesia                             |
| Arak                       | Iran                                  |
| Esfahan                    | Iran                                  |
| Kermanshah                 | Iran                                  |
| Najafabad                  | Iran                                  |
| Qomsheh                    | Iran                                  |
| Shahr-e Kord               | Iran                                  |
| Sirjan                     | Iran                                  |
| Tabriz                     | Iran                                  |
| Mosul                      | Iraq                                  |
| Ashdod                     | Israel                                |
| Ashqelon                   | Israel                                |
| Bat Yam                    | Israel                                |
| Tel Aviv-Jaffa             | Israel                                |
| Alessandria                | Italy                                 |
| Bergamo                    | Italy                                 |
| Brescia                    | Italy                                 |
| Brindisi                   | Italy                                 |
| Livorno                    | Italy                                 |
| Syrakusa                   | Italy                                 |
| Udine                      | Italy                                 |
| Akishima                   | Japan                                 |
| Fukuyama                   | Japan                                 |
| Higashiosaka               | Japan                                 |
| Hino                       | Japan                                 |
| Hiroshima                  | Japan                                 |
| Isesaki                    | Japan                                 |
| Iwaki                      | Japan                                 |
| Iwakuni                    | Japan                                 |
| Iwatsuki                   | Japan                                 |
| Izumisano                  | Japan                                 |
| Kakamigahara               | Japan                                 |
| Kamakura                   | Japan                                 |
| Kanazawa                   | Japan                                 |
| Koriyama                   | Japan                                 |
| Kurashiki                  | Japan                                 |
| Kuwana                     | Japan                                 |
| Matsue                     | Japan                                 |
| Miyakonojo                 | Japan                                 |
| Nagareyama                 | Japan                                 |
| Okayama                    | Japan                                 |
| Okinawa                    | Japan                                 |
| Omiya                      | Japan                                 |
| Onomichi                   | Japan                                 |
| Otsu                       | Japan                                 |
| Sagamihara                 | Japan                                 |
| Sasebo                     | Japan                                 |
| Shimonoseki                | Japan                                 |
| Tama                       | Japan                                 |
| Tsuyama                    | Japan                                 |
| Ueda                       | Japan                                 |
| Urawa                      | Japan                                 |
| Pavlodar                   | Kazakstan                             |
| Zhezqazghan                | Kazakstan                             |
| Kisumu                     | Kenya                                 |
| Nyeri                      | Kenya                                 |
| Jalib al-Shuyukh           | Kuwait                                |
| Daugavpils                 | Latvia                                |
| Liepaja                    | Latvia                                |
| Vaduz                      | Liechtenstein                         |
| Vilnius                    | Lithuania                             |
| Mahajanga                  | Madagascar                            |
| Lilongwe                   | Malawi                                |
| Ipoh                       | Malaysia                              |
| Kuching                    | Malaysia                              |
| Sungai Petani              | Malaysia                              |
| Acua                       | Mexico                                |
| Allende                    | Mexico                                |
| Atlixco                    | Mexico                                |
| Carmen                     | Mexico                                |
| Celaya                     | Mexico                                |
| Coacalco de Berriozbal     | Mexico                                |
| Coatzacoalcos              | Mexico                                |
| Cuauhtmoc                  | Mexico                                |
| Cuautla                    | Mexico                                |
| Cuernavaca                 | Mexico                                |
| El Fuerte                  | Mexico                                |
| Guadalajara                | Mexico                                |
| Hidalgo                    | Mexico                                |
| Huejutla de Reyes          | Mexico                                |
| Huixquilucan               | Mexico                                |
| Jos Azueta                 | Mexico                                |
| Jurez                      | Mexico                                |
| La Paz                     | Mexico                                |
| Matamoros                  | Mexico                                |
| Mexicali                   | Mexico                                |
| Monclova                   | Mexico                                |
| Nezahualcyotl              | Mexico                                |
| Pachuca de Soto            | Mexico                                |
| Salamanca                  | Mexico                                |
| San Felipe del Progreso    | Mexico                                |
| San Juan Bautista Tuxtepec | Mexico                                |
| Torren                     | Mexico                                |
| Uruapan                    | Mexico                                |
| Valle de Santiago          | Mexico                                |
| Zapopan                    | Mexico                                |
| Chisinau                   | Moldova                               |
| Beni-Mellal                | Morocco                               |
| Nador                      | Morocco                               |
| Sal                        | Morocco                               |
| Beira                      | Mozambique                            |
| Naala-Porto                | Mozambique                            |
| Tete                       | Mozambique                            |
| Monywa                     | Myanmar                               |
| Myingyan                   | Myanmar                               |
| Yangor                     | Nauru                                 |
| Birgunj                    | Nepal                                 |
| Amersfoort                 | Netherlands                           |
| Apeldoorn                  | Netherlands                           |
| Ede                        | Netherlands                           |
| Emmen                      | Netherlands                           |
| s-Hertogenbosch            | Netherlands                           |
| Hamilton                   | New Zealand                           |
| Benin City                 | Nigeria                               |
| Deba Habe                  | Nigeria                               |
| Effon-Alaiye               | Nigeria                               |
| Ife                        | Nigeria                               |
| Ikerre                     | Nigeria                               |
| Ilorin                     | Nigeria                               |
| Kaduna                     | Nigeria                               |
| Ogbomosho                  | Nigeria                               |
| Ondo                       | Nigeria                               |
| Owo                        | Nigeria                               |
| Oyo                        | Nigeria                               |
| Sokoto                     | Nigeria                               |
| Zaria                      | Nigeria                               |
| Pyongyang                  | North Korea                           |
| Masqat                     | Oman                                  |
| Salala                     | Oman                                  |
| Dadu                       | Pakistan                              |
| Mandi Bahauddin            | Pakistan                              |
| Mardan                     | Pakistan                              |
| Okara                      | Pakistan                              |
| Shikarpur                  | Pakistan                              |
| Asuncin                    | Paraguay                              |
| Ciudad del Este            | Paraguay                              |
| San Lorenzo                | Paraguay                              |
| Callao                     | Peru                                  |
| Hunuco                     | Peru                                  |
| Lima                       | Peru                                  |
| Sullana                    | Peru                                  |
| Baybay                     | Philippines                           |
| Bayugan                    | Philippines                           |
| Bislig                     | Philippines                           |
| Cabuyao                    | Philippines                           |
| Cavite                     | Philippines                           |
| Davao                      | Philippines                           |
| Gingoog                    | Philippines                           |
| Hagonoy                    | Philippines                           |
| Iligan                     | Philippines                           |
| Imus                       | Philippines                           |
| Lapu-Lapu                  | Philippines                           |
| Mandaluyong                | Philippines                           |
| Ozamis                     | Philippines                           |
| Santa Rosa                 | Philippines                           |
| Taguig                     | Philippines                           |
| Talavera                   | Philippines                           |
| Tanauan                    | Philippines                           |
| Tanza                      | Philippines                           |
| Tarlac                     | Philippines                           |
| Tuguegarao                 | Philippines                           |
| Bydgoszcz                  | Poland                                |
| Czestochowa                | Poland                                |
| Jastrzebie-Zdrj            | Poland                                |
| Kalisz                     | Poland                                |
| Lublin                     | Poland                                |
| Plock                      | Poland                                |
| Tychy                      | Poland                                |
| Wroclaw                    | Poland                                |
| Arecibo                    | Puerto Rico                           |
| Ponce                      | Puerto Rico                           |
| Botosani                   | Romania                               |
| Bucuresti                  | Romania                               |
| Saint-Denis                | Runion                                |
| Atinsk                     | Russian Federation                    |
| Balaiha                    | Russian Federation                    |
| Dzerzinsk                  | Russian Federation                    |
| Elista                     | Russian Federation                    |
| Ivanovo                    | Russian Federation                    |
| Jaroslavl                  | Russian Federation                    |
| Jelets                     | Russian Federation                    |
| Kaliningrad                | Russian Federation                    |
| Kamyin                     | Russian Federation                    |
| Kirovo-Tepetsk             | Russian Federation                    |
| Kolpino                    | Russian Federation                    |
| Korolev                    | Russian Federation                    |
| Kurgan                     | Russian Federation                    |
| Kursk                      | Russian Federation                    |
| Lipetsk                    | Russian Federation                    |
| Ljubertsy                  | Russian Federation                    |
| Maikop                     | Russian Federation                    |
| Moscow                     | Russian Federation                    |
| Nabereznyje Telny          | Russian Federation                    |
| Niznekamsk                 | Russian Federation                    |
| Novoterkassk               | Russian Federation                    |
| Pjatigorsk                 | Russian Federation                    |
| Serpuhov                   | Russian Federation                    |
| Smolensk                   | Russian Federation                    |
| Syktyvkar                  | Russian Federation                    |
| Teboksary                  | Russian Federation                    |
| Usolje-Sibirskoje          | Russian Federation                    |
| Zeleznogorsk               | Russian Federation                    |
| Kingstown                  | Saint Vincent and the Grenadines      |
| Abha                       | Saudi Arabia                          |
| al-Hawiya                  | Saudi Arabia                          |
| al-Qatif                   | Saudi Arabia                          |
| Jedda                      | Saudi Arabia                          |
| Tabuk                      | Saudi Arabia                          |
| Ziguinchor                 | Senegal                               |
| Bratislava                 | Slovakia                              |
| Boksburg                   | South Africa                          |
| Botshabelo                 | South Africa                          |
| Chatsworth                 | South Africa                          |
| Johannesburg               | South Africa                          |
| Kimberley                  | South Africa                          |
| Klerksdorp                 | South Africa                          |
| Newcastle                  | South Africa                          |
| Paarl                      | South Africa                          |
| Rustenburg                 | South Africa                          |
| Soshanguve                 | South Africa                          |
| Springs                    | South Africa                          |
| Cheju                      | South Korea                           |
| Kimchon                    | South Korea                           |
| Naju                       | South Korea                           |
| Tonghae                    | South Korea                           |
| Uijongbu                   | South Korea                           |
| A Corua (La Corua)         | Spain                                 |
| Donostia-San Sebastin      | Spain                                 |
| Gijn                       | Spain                                 |
| Ourense (Orense)           | Spain                                 |
| Santiago de Compostela     | Spain                                 |
| Jaffna                     | Sri Lanka                             |
| al-Qadarif                 | Sudan                                 |
| Omdurman                   | Sudan                                 |
| Malm                       | Sweden                                |
| Basel                      | Switzerland                           |
| Bern                       | Switzerland                           |
| Lausanne                   | Switzerland                           |
| Changhwa                   | Taiwan                                |
| Chiayi                     | Taiwan                                |
| Chungho                    | Taiwan                                |
| Fengshan                   | Taiwan                                |
| Hsichuh                    | Taiwan                                |
| Lungtan                    | Taiwan                                |
| Nantou                     | Taiwan                                |
| Tanshui                    | Taiwan                                |
| Touliu                     | Taiwan                                |
| Tsaotun                    | Taiwan                                |
| Mwanza                     | Tanzania                              |
| Tabora                     | Tanzania                              |
| Zanzibar                   | Tanzania                              |
| Nakhon Sawan               | Thailand                              |
| Pak Kret                   | Thailand                              |
| Songkhla                   | Thailand                              |
| Nukualofa                  | Tonga                                 |
| Sousse                     | Tunisia                               |
| Adana                      | Turkey                                |
| Balikesir                  | Turkey                                |
| Batman                     | Turkey                                |
| Denizli                    | Turkey                                |
| Eskisehir                  | Turkey                                |
| Gaziantep                  | Turkey                                |
| Inegl                      | Turkey                                |
| Kilis                      | Turkey                                |
| Ktahya                     | Turkey                                |
| Osmaniye                   | Turkey                                |
| Sivas                      | Turkey                                |
| Sultanbeyli                | Turkey                                |
| Tarsus                     | Turkey                                |
| Tokat                      | Turkey                                |
| Usak                       | Turkey                                |
| Ashgabat                   | Turkmenistan                          |
| Funafuti                   | Tuvalu                                |
| Kamjanets-Podilskyi        | Ukraine                               |
| Konotop                    | Ukraine                               |
| Mukateve                   | Ukraine                               |
| ostka                      | Ukraine                               |
| Simferopol                 | Ukraine                               |
| Sumy                       | Ukraine                               |
| Abu Dhabi                  | United Arab Emirates                  |
| al-Ayn                     | United Arab Emirates                  |
| Sharja                     | United Arab Emirates                  |
| Bradford                   | United Kingdom                        |
| Dundee                     | United Kingdom                        |
| London                     | United Kingdom                        |
| Southampton                | United Kingdom                        |
| Southend-on-Sea            | United Kingdom                        |
| Southport                  | United Kingdom                        |
| Stockport                  | United Kingdom                        |
| York                       | United Kingdom                        |
| Akron                      | United States                         |
| Arlington                  | United States                         |
| Augusta-Richmond County    | United States                         |
| Aurora                     | United States                         |
| Bellevue                   | United States                         |
| Brockton                   | United States                         |
| Cape Coral                 | United States                         |
| Citrus Heights             | United States                         |
| Clarksville                | United States                         |
| Compton                    | United States                         |
| Dallas                     | United States                         |
| Dayton                     | United States                         |
| El Monte                   | United States                         |
| Fontana                    | United States                         |
| Garden Grove               | United States                         |
| Garland                    | United States                         |
| Grand Prairie              | United States                         |
| Greensboro                 | United States                         |
| Joliet                     | United States                         |
| Kansas City                | United States                         |
| Lancaster                  | United States                         |
| Laredo                     | United States                         |
| Lincoln                    | United States                         |
| Manchester                 | United States                         |
| Memphis                    | United States                         |
| Peoria                     | United States                         |
| Roanoke                    | United States                         |
| Rockford                   | United States                         |
| Saint Louis                | United States                         |
| Salinas                    | United States                         |
| San Bernardino             | United States                         |
| Sterling Heights           | United States                         |
| Sunnyvale                  | United States                         |
| Tallahassee                | United States                         |
| Warren                     | United States                         |
| Barcelona                  | Venezuela                             |
| Caracas                    | Venezuela                             |
| Cuman                      | Venezuela                             |
| Maracabo                   | Venezuela                             |
| Ocumare del Tuy            | Venezuela                             |
| Valencia                   | Venezuela                             |
| Valle de la Pascua         | Venezuela                             |
| Cam Ranh                   | Vietnam                               |
| Haiphong                   | Vietnam                               |
| Hanoi                      | Vietnam                               |
| Nam Dinh                   | Vietnam                               |
| Nha Trang                  | Vietnam                               |
| Vinh                       | Vietnam                               |
| Charlotte Amalie           | Virgin Islands, U.S.                  |
| Aden                       | Yemen                                 |
| Hodeida                    | Yemen                                 |
| Sanaa                      | Yemen                                 |
| Taizz                      | Yemen                                 |
| Kragujevac                 | Yugoslavia                            |
| Novi Sad                   | Yugoslavia                            |
| Kitwe                      | Zambia                                |
+----------------------------+---------------------------------------+
600 rows in set (0,00 sec)
   ```

5. Obtener los detalles de los alquileres, incluyendo el cliente y el
empleado que gestionó el alquiler.

```mysql
SELECT 
	a.id_alquiler,
	c.nombre,
	e.nombre 
FROM
	alquiler AS a 
JOIN 
	cliente AS c ON c.id_cliente = a.id_cliente 
JOIN 
	empleado AS e ON e.id_empleado = a.id_empleado ;
	
--------------------------------------
|       15725 | AUSTIN      | Mike   |
+-------------+-------------+--------+
16045 rows in set (0,04 sec)
   ```

6. Encontrar todas las películas que se encuentran en un almacén
específico.

```mysql
select p.titulo, a.id_almacen
from pelicula as p
inner join inventario as i ON i.id_pelicula = p.id_pelicula
inner join almacen as a ON a.id_almacen = i.id_almacen
WHERE a.id_almacen = 1

| titulo                      | id_almacen |
+-----------------------------+------------+
| ACADEMY DINOSAUR            |          1 |
| ACADEMY DINOSAUR            |          1 |
| ACADEMY DINOSAUR            |          1 |
| ACADEMY DINOSAUR            |          1 |
| AFFAIR PREJUDICE            |          1 |
| AFFAIR PREJUDICE            |          1 |
| AFFAIR PREJUDICE            |          1 |
| AFFAIR PREJUDICE            |          1 |
| AGENT TRUMAN                |          1 |
| AGENT TRUMAN                |          1 |
| AGENT TRUMAN                |          1 |
| AIRPLANE SIERRA             |          1 |
| AIRPLANE SIERRA             |          1 |
| ALABAMA DEVIL               |          1 |
| ALABAMA DEVIL               |          1 |
| ALABAMA DEVIL               |          1 |
| ALADDIN CALENDAR            |          1 |
| ALADDIN CALENDAR            |          1 |
| ALADDIN CALENDAR            |          1 |
| ALADDIN CALENDAR            |          1 |
| ALAMO VIDEOTAPE             |          1 |
| ALAMO VIDEOTAPE             |          1 |
| ALAMO VIDEOTAPE             |          1 |
| ALAMO VIDEOTAPE             |          1 |
| ALASKA PHANTOM              |          1 |
| ALASKA PHANTOM              |          1 |
| ALASKA PHANTOM              |          1 |
| ALIEN CENTER                |          1 |
| ALIEN CENTER                |          1 |
| ALLEY EVOLUTION             |          1 |
| ALLEY EVOLUTION             |          1 |
| ALONE TRIP                  |          1 |
| ALONE TRIP                  |          1 |
| ALONE TRIP                  |          1 |
| ALTER VICTORY               |          1 |
| ALTER VICTORY               |          1 |
| ALTER VICTORY               |          1 |
| AMADEUS HOLY                |          1 |
| AMADEUS HOLY                |          1 |
| AMADEUS HOLY                |          1 |
| AMADEUS HOLY                |          1 |
| AMELIE HELLFIGHTERS         |          1 |
| AMELIE HELLFIGHTERS         |          1 |
| AMELIE HELLFIGHTERS         |          1 |
| AMERICAN CIRCUS             |          1 |
| AMERICAN CIRCUS             |          1 |
| AMISTAD MIDSUMMER           |          1 |
| AMISTAD MIDSUMMER           |          1 |
| AMISTAD MIDSUMMER           |          1 |
| AMISTAD MIDSUMMER           |          1 |
| ANACONDA CONFESSIONS        |          1 |
| ANACONDA CONFESSIONS        |          1 |
| ANACONDA CONFESSIONS        |          1 |
| ANALYZE HOOSIERS            |          1 |
| ANALYZE HOOSIERS            |          1 |
| ANALYZE HOOSIERS            |          1 |
| ANALYZE HOOSIERS            |          1 |
| ANGELS LIFE                 |          1 |
| ANGELS LIFE                 |          1 |
| ANGELS LIFE                 |          1 |
| ANGELS LIFE                 |          1 |
| ANNIE IDENTITY              |          1 |
| ANNIE IDENTITY              |          1 |
| ANONYMOUS HUMAN             |          1 |
| ANONYMOUS HUMAN             |          1 |
| ANONYMOUS HUMAN             |          1 |
| ANONYMOUS HUMAN             |          1 |
| ANTHEM LUKE                 |          1 |
| ANTHEM LUKE                 |          1 |
| ANTHEM LUKE                 |          1 |
| ANTITRUST TOMATOES          |          1 |
| ANTITRUST TOMATOES          |          1 |
| ANYTHING SAVANNAH           |          1 |
| ANYTHING SAVANNAH           |          1 |
| APACHE DIVINE               |          1 |
| APACHE DIVINE               |          1 |
| APACHE DIVINE               |          1 |
| APACHE DIVINE               |          1 |
| ARACHNOPHOBIA ROLLERCOASTER |          1 |
| ARACHNOPHOBIA ROLLERCOASTER |          1 |
| ARACHNOPHOBIA ROLLERCOASTER |          1 |
| ARACHNOPHOBIA ROLLERCOASTER |          1 |
| ARIZONA BANG                |          1 |
| ARIZONA BANG                |          1 |
| ARIZONA BANG                |          1 |
| ARIZONA BANG                |          1 |
| ARMAGEDDON LOST             |          1 |
| ARMAGEDDON LOST             |          1 |
| ARMAGEDDON LOST             |          1 |
| ATLANTIS CAUSE              |          1 |
| ATLANTIS CAUSE              |          1 |
| ATLANTIS CAUSE              |          1 |
| ATTACKS HATE                |          1 |
| ATTACKS HATE                |          1 |
| ATTRACTION NEWTON           |          1 |
| ATTRACTION NEWTON           |          1 |
| ATTRACTION NEWTON           |          1 |
| ATTRACTION NEWTON           |          1 |
| BACKLASH UNDEFEATED         |          1 |
| BACKLASH UNDEFEATED         |          1 |
| BADMAN DAWN                 |          1 |
| BADMAN DAWN                 |          1 |
| BADMAN DAWN                 |          1 |
| BAKED CLEOPATRA             |          1 |
| BAKED CLEOPATRA             |          1 |
| BAKED CLEOPATRA             |          1 |
| BALLOON HOMEWARD            |          1 |
| BALLOON HOMEWARD            |          1 |
| BANG KWAI                   |          1 |
| BANG KWAI                   |          1 |
| BANGER PINOCCHIO            |          1 |
| BANGER PINOCCHIO            |          1 |
| BANGER PINOCCHIO            |          1 |
| BARBARELLA STREETCAR        |          1 |
| BARBARELLA STREETCAR        |          1 |
| BARBARELLA STREETCAR        |          1 |
| BARBARELLA STREETCAR        |          1 |
| BAREFOOT MANCHURIAN         |          1 |
| BAREFOOT MANCHURIAN         |          1 |
| BAREFOOT MANCHURIAN         |          1 |
| BASIC EASY                  |          1 |
| BASIC EASY                  |          1 |
| BASIC EASY                  |          1 |
| BASIC EASY                  |          1 |
| BEAR GRACELAND              |          1 |
| BEAR GRACELAND              |          1 |
| BEAR GRACELAND              |          1 |
| BEAST HUNCHBACK             |          1 |
| BEAST HUNCHBACK             |          1 |
| BEAST HUNCHBACK             |          1 |
| BEAUTY GREASE               |          1 |
| BEAUTY GREASE               |          1 |
| BEAUTY GREASE               |          1 |
| BEAUTY GREASE               |          1 |
| BEDAZZLED MARRIED           |          1 |
| BEDAZZLED MARRIED           |          1 |
| BENEATH RUSH                |          1 |
| BENEATH RUSH                |          1 |
| BENEATH RUSH                |          1 |
| BERETS AGENT                |          1 |
| BERETS AGENT                |          1 |
| BETRAYED REAR               |          1 |
| BETRAYED REAR               |          1 |
| BEVERLY OUTLAW              |          1 |
| BEVERLY OUTLAW              |          1 |
| BEVERLY OUTLAW              |          1 |
| BEVERLY OUTLAW              |          1 |
| BIKINI BORROWERS            |          1 |
| BIKINI BORROWERS            |          1 |
| BILL OTHERS                 |          1 |
| BILL OTHERS                 |          1 |
| BILL OTHERS                 |          1 |
| BILL OTHERS                 |          1 |
| BINGO TALENTED              |          1 |
| BINGO TALENTED              |          1 |
| BINGO TALENTED              |          1 |
| BINGO TALENTED              |          1 |
| BIRCH ANTITRUST             |          1 |
| BIRCH ANTITRUST             |          1 |
| BIRCH ANTITRUST             |          1 |
| BIRDCAGE CASPER             |          1 |
| BIRDCAGE CASPER             |          1 |
| BIRDCAGE CASPER             |          1 |
| BIRDS PERDITION             |          1 |
| BIRDS PERDITION             |          1 |
| BIRDS PERDITION             |          1 |
| BIRDS PERDITION             |          1 |
| BLACKOUT PRIVATE            |          1 |
| BLACKOUT PRIVATE            |          1 |
| BLACKOUT PRIVATE            |          1 |
| BLADE POLISH                |          1 |
| BLADE POLISH                |          1 |
| BLADE POLISH                |          1 |
| BLANKET BEVERLY             |          1 |
| BLANKET BEVERLY             |          1 |
| BLANKET BEVERLY             |          1 |
| BLANKET BEVERLY             |          1 |
| BLINDNESS GUN               |          1 |
| BLINDNESS GUN               |          1 |
| BLINDNESS GUN               |          1 |
| BLINDNESS GUN               |          1 |
| BLOOD ARGONAUTS             |          1 |
| BLOOD ARGONAUTS             |          1 |
| BLUES INSTINCT              |          1 |
| BLUES INSTINCT              |          1 |
| BLUES INSTINCT              |          1 |
| BOILED DARES                |          1 |
| BOILED DARES                |          1 |
| BOILED DARES                |          1 |
| BOILED DARES                |          1 |
| BOOGIE AMELIE               |          1 |
| BOOGIE AMELIE               |          1 |
| BOOGIE AMELIE               |          1 |
| BOOGIE AMELIE               |          1 |
| BORROWERS BEDAZZLED         |          1 |
| BORROWERS BEDAZZLED         |          1 |
| BORROWERS BEDAZZLED         |          1 |
| BOULEVARD MOB               |          1 |
| BOULEVARD MOB               |          1 |
| BOULEVARD MOB               |          1 |
| BOUND CHEAPER               |          1 |
| BOUND CHEAPER               |          1 |
| BOUND CHEAPER               |          1 |
| BOUND CHEAPER               |          1 |
| BOWFINGER GABLES            |          1 |
| BOWFINGER GABLES            |          1 |
| BRAVEHEART HUMAN            |          1 |
| BRAVEHEART HUMAN            |          1 |
| BREAKFAST GOLDFINGER        |          1 |
| BREAKFAST GOLDFINGER        |          1 |
| BREAKING HOME               |          1 |
| BREAKING HOME               |          1 |
| BREAKING HOME               |          1 |
| BRIDE INTRIGUE              |          1 |
| BRIDE INTRIGUE              |          1 |
| BRIDE INTRIGUE              |          1 |
| BRIDE INTRIGUE              |          1 |
| BRIGHT ENCOUNTERS           |          1 |
| BRIGHT ENCOUNTERS           |          1 |
| BRIGHT ENCOUNTERS           |          1 |
| BRINGING HYSTERICAL         |          1 |
| BRINGING HYSTERICAL         |          1 |
| BRINGING HYSTERICAL         |          1 |
| BROOKLYN DESERT             |          1 |
| BROOKLYN DESERT             |          1 |
| BROOKLYN DESERT             |          1 |
| BROOKLYN DESERT             |          1 |
| BROTHERHOOD BLANKET         |          1 |
| BROTHERHOOD BLANKET         |          1 |
| BROTHERHOOD BLANKET         |          1 |
| BROTHERHOOD BLANKET         |          1 |
| BUCKET BROTHERHOOD          |          1 |
| BUCKET BROTHERHOOD          |          1 |
| BUCKET BROTHERHOOD          |          1 |
| BUCKET BROTHERHOOD          |          1 |
| BULL SHAWSHANK              |          1 |
| BULL SHAWSHANK              |          1 |
| BULWORTH COMMANDMENTS       |          1 |
| BULWORTH COMMANDMENTS       |          1 |
| BUTTERFLY CHOCOLAT          |          1 |
| BUTTERFLY CHOCOLAT          |          1 |
| BUTTERFLY CHOCOLAT          |          1 |
| BUTTERFLY CHOCOLAT          |          1 |
| CABIN FLASH                 |          1 |
| CABIN FLASH                 |          1 |
| CABIN FLASH                 |          1 |
| CABIN FLASH                 |          1 |
| CALENDAR GUNFIGHT           |          1 |
| CALENDAR GUNFIGHT           |          1 |
| CALENDAR GUNFIGHT           |          1 |
| CALENDAR GUNFIGHT           |          1 |
| CAMELOT VACATION            |          1 |
| CAMELOT VACATION            |          1 |
| CAMELOT VACATION            |          1 |
| CAMELOT VACATION            |          1 |
| CAMPUS REMEMBER             |          1 |
| CAMPUS REMEMBER             |          1 |
| CAMPUS REMEMBER             |          1 |
| CANDIDATE PERDITION         |          1 |
| CANDIDATE PERDITION         |          1 |
| CANDLES GRAPES              |          1 |
| CANDLES GRAPES              |          1 |
| CANDLES GRAPES              |          1 |
| CANDLES GRAPES              |          1 |
| CANYON STOCK                |          1 |
| CANYON STOCK                |          1 |
| CANYON STOCK                |          1 |
| CANYON STOCK                |          1 |
| CAPER MOTIONS               |          1 |
| CAPER MOTIONS               |          1 |
| CAPER MOTIONS               |          1 |
| CARIBBEAN LIBERTY           |          1 |
| CARIBBEAN LIBERTY           |          1 |
| CARIBBEAN LIBERTY           |          1 |
| CAROL TEXAS                 |          1 |
| CAROL TEXAS                 |          1 |
| CAROL TEXAS                 |          1 |
| CARRIE BUNCH                |          1 |
| CARRIE BUNCH                |          1 |
| CARRIE BUNCH                |          1 |
| CARRIE BUNCH                |          1 |
| CASABLANCA SUPER            |          1 |
| CASABLANCA SUPER            |          1 |
| CAT CONEHEADS               |          1 |
| CAT CONEHEADS               |          1 |
| CAT CONEHEADS               |          1 |
| CAT CONEHEADS               |          1 |
| CAUSE DATE                  |          1 |
| CAUSE DATE                  |          1 |
| CAUSE DATE                  |          1 |
| CELEBRITY HORN              |          1 |
| CELEBRITY HORN              |          1 |
| CENTER DINOSAUR             |          1 |
| CENTER DINOSAUR             |          1 |
| CENTER DINOSAUR             |          1 |
| CENTER DINOSAUR             |          1 |
| CHAINSAW UPTOWN             |          1 |
| CHAINSAW UPTOWN             |          1 |
| CHAINSAW UPTOWN             |          1 |
| CHAINSAW UPTOWN             |          1 |
| CHAMBER ITALIAN             |          1 |
| CHAMBER ITALIAN             |          1 |
| CHANCE RESURRECTION         |          1 |
| CHANCE RESURRECTION         |          1 |
| CHANCE RESURRECTION         |          1 |
| CHAPLIN LICENSE             |          1 |
| CHAPLIN LICENSE             |          1 |
| CHAPLIN LICENSE             |          1 |
| CHARIOTS CONSPIRACY         |          1 |
| CHARIOTS CONSPIRACY         |          1 |
| CHASING FIGHT               |          1 |
| CHASING FIGHT               |          1 |
| CHASING FIGHT               |          1 |
| CHASING FIGHT               |          1 |
| CHEAPER CLYDE               |          1 |
| CHEAPER CLYDE               |          1 |
| CHICAGO NORTH               |          1 |
| CHICAGO NORTH               |          1 |
| CHICAGO NORTH               |          1 |
| CHICKEN HELLFIGHTERS        |          1 |
| CHICKEN HELLFIGHTERS        |          1 |
| CHICKEN HELLFIGHTERS        |          1 |
| CHILL LUCK                  |          1 |
| CHILL LUCK                  |          1 |
| CHILL LUCK                  |          1 |
| CHILL LUCK                  |          1 |
| CHITTY LOCK                 |          1 |
| CHITTY LOCK                 |          1 |
| CHITTY LOCK                 |          1 |
| CHOCOLAT HARRY              |          1 |
| CHOCOLAT HARRY              |          1 |
| CHOCOLAT HARRY              |          1 |
| CHRISTMAS MOONSHINE         |          1 |
| CHRISTMAS MOONSHINE         |          1 |
| CHRISTMAS MOONSHINE         |          1 |
| CIDER DESIRE                |          1 |
| CIDER DESIRE                |          1 |
| CINCINATTI WHISPERER        |          1 |
| CINCINATTI WHISPERER        |          1 |
| CIRCUS YOUTH                |          1 |
| CIRCUS YOUTH                |          1 |
| CIRCUS YOUTH                |          1 |
| CIRCUS YOUTH                |          1 |
| CITIZEN SHREK               |          1 |
| CITIZEN SHREK               |          1 |
| CITIZEN SHREK               |          1 |
| CITIZEN SHREK               |          1 |
| CLASH FREDDY                |          1 |
| CLASH FREDDY                |          1 |
| CLASH FREDDY                |          1 |
| CLEOPATRA DEVIL             |          1 |
| CLEOPATRA DEVIL             |          1 |
| CLONES PINOCCHIO            |          1 |
| CLONES PINOCCHIO            |          1 |
| CLOSER BANG                 |          1 |
| CLOSER BANG                 |          1 |
| CLOSER BANG                 |          1 |
| CLOSER BANG                 |          1 |
| CLUB GRAFFITI               |          1 |
| CLUB GRAFFITI               |          1 |
| CLUE GRAIL                  |          1 |
| CLUE GRAIL                  |          1 |
| CLUELESS BUCKET             |          1 |
| CLUELESS BUCKET             |          1 |
| CLUELESS BUCKET             |          1 |
| COAST RAINBOW               |          1 |
| COAST RAINBOW               |          1 |
| COLDBLOODED DARLING         |          1 |
| COLDBLOODED DARLING         |          1 |
| COLDBLOODED DARLING         |          1 |
| COLOR PHILADELPHIA          |          1 |
| COLOR PHILADELPHIA          |          1 |
| COLOR PHILADELPHIA          |          1 |
| COLOR PHILADELPHIA          |          1 |
| COMA HEAD                   |          1 |
| COMA HEAD                   |          1 |
| COMA HEAD                   |          1 |
| COMA HEAD                   |          1 |
| COMANCHEROS ENEMY           |          1 |
| COMANCHEROS ENEMY           |          1 |
| COMFORTS RUSH               |          1 |
| COMFORTS RUSH               |          1 |
| COMMAND DARLING             |          1 |
| COMMAND DARLING             |          1 |
| CONEHEADS SMOOCHY           |          1 |
| CONEHEADS SMOOCHY           |          1 |
| CONEHEADS SMOOCHY           |          1 |
| CONEHEADS SMOOCHY           |          1 |
| CONFESSIONS MAGUIRE         |          1 |
| CONFESSIONS MAGUIRE         |          1 |
| CONFESSIONS MAGUIRE         |          1 |
| CONFIDENTIAL INTERVIEW      |          1 |
| CONFIDENTIAL INTERVIEW      |          1 |
| CONFIDENTIAL INTERVIEW      |          1 |
| CONFIDENTIAL INTERVIEW      |          1 |
| CONFUSED CANDLES            |          1 |
| CONFUSED CANDLES            |          1 |
| CONGENIALITY QUEST          |          1 |
| CONGENIALITY QUEST          |          1 |
| CONNECTION MICROCOSMOS      |          1 |
| CONNECTION MICROCOSMOS      |          1 |
| CONQUERER NUTS              |          1 |
| CONQUERER NUTS              |          1 |
| CONQUERER NUTS              |          1 |
| CONQUERER NUTS              |          1 |
| CONTACT ANONYMOUS           |          1 |
| CONTACT ANONYMOUS           |          1 |
| CONTACT ANONYMOUS           |          1 |
| CONTROL ANTHEM              |          1 |
| CONTROL ANTHEM              |          1 |
| CONVERSATION DOWNHILL       |          1 |
| CONVERSATION DOWNHILL       |          1 |
| CONVERSATION DOWNHILL       |          1 |
| CORE SUIT                   |          1 |
| CORE SUIT                   |          1 |
| COWBOY DOOM                 |          1 |
| COWBOY DOOM                 |          1 |
| CRAFT OUTFIELD              |          1 |
| CRAFT OUTFIELD              |          1 |
| CRAZY HOME                  |          1 |
| CRAZY HOME                  |          1 |
| CRAZY HOME                  |          1 |
| CREATURES SHAKESPEARE       |          1 |
| CREATURES SHAKESPEARE       |          1 |
| CROOKED FROGMEN             |          1 |
| CROOKED FROGMEN             |          1 |
| CROOKED FROGMEN             |          1 |
| CROSSROADS CASUALTIES       |          1 |
| CROSSROADS CASUALTIES       |          1 |
| CROSSROADS CASUALTIES       |          1 |
| CROSSROADS CASUALTIES       |          1 |
| CROW GREASE                 |          1 |
| CROW GREASE                 |          1 |
| CRUELTY UNFORGIVEN          |          1 |
| CRUELTY UNFORGIVEN          |          1 |
| CRUSADE HONEY               |          1 |
| CRUSADE HONEY               |          1 |
| CUPBOARD SINNERS            |          1 |
| CUPBOARD SINNERS            |          1 |
| CUPBOARD SINNERS            |          1 |
| CUPBOARD SINNERS            |          1 |
| CURTAIN VIDEOTAPE           |          1 |
| CURTAIN VIDEOTAPE           |          1 |
| CURTAIN VIDEOTAPE           |          1 |
| CURTAIN VIDEOTAPE           |          1 |
| CYCLONE FAMILY              |          1 |
| CYCLONE FAMILY              |          1 |
| CYCLONE FAMILY              |          1 |
| CYCLONE FAMILY              |          1 |
| DADDY PITTSBURGH            |          1 |
| DADDY PITTSBURGH            |          1 |
| DADDY PITTSBURGH            |          1 |
| DALMATIONS SWEDEN           |          1 |
| DALMATIONS SWEDEN           |          1 |
| DALMATIONS SWEDEN           |          1 |
| DALMATIONS SWEDEN           |          1 |
| DANCES NONE                 |          1 |
| DANCES NONE                 |          1 |
| DANCES NONE                 |          1 |
| DANCES NONE                 |          1 |
| DANCING FEVER               |          1 |
| DANCING FEVER               |          1 |
| DANCING FEVER               |          1 |
| DANCING FEVER               |          1 |
| DANGEROUS UPTOWN            |          1 |
| DANGEROUS UPTOWN            |          1 |
| DANGEROUS UPTOWN            |          1 |
| DANGEROUS UPTOWN            |          1 |
| DARES PLUTO                 |          1 |
| DARES PLUTO                 |          1 |
| DARES PLUTO                 |          1 |
| DARKNESS WAR                |          1 |
| DARKNESS WAR                |          1 |
| DARKNESS WAR                |          1 |
| DARKNESS WAR                |          1 |
| DARLING BREAKING            |          1 |
| DARLING BREAKING            |          1 |
| DARN FORRESTER              |          1 |
| DARN FORRESTER              |          1 |
| DARN FORRESTER              |          1 |
| DATE SPEED                  |          1 |
| DATE SPEED                  |          1 |
| DATE SPEED                  |          1 |
| DATE SPEED                  |          1 |
| DAWN POND                   |          1 |
| DAWN POND                   |          1 |
| DAWN POND                   |          1 |
| DAY UNFAITHFUL              |          1 |
| DAY UNFAITHFUL              |          1 |
| DECEIVER BETRAYED           |          1 |
| DECEIVER BETRAYED           |          1 |
| DECEIVER BETRAYED           |          1 |
| DECEIVER BETRAYED           |          1 |
| DEEP CRUSADE                |          1 |
| DEEP CRUSADE                |          1 |
| DEEP CRUSADE                |          1 |
| DEEP CRUSADE                |          1 |
| DEER VIRGINIAN              |          1 |
| DEER VIRGINIAN              |          1 |
| DEER VIRGINIAN              |          1 |
| DEER VIRGINIAN              |          1 |
| DESERT POSEIDON             |          1 |
| DESERT POSEIDON             |          1 |
| DESPERATE TRAINSPOTTING     |          1 |
| DESPERATE TRAINSPOTTING     |          1 |
| DESTINATION JERK            |          1 |
| DESTINATION JERK            |          1 |
| DESTINATION JERK            |          1 |
| DESTINY SATURDAY            |          1 |
| DESTINY SATURDAY            |          1 |
| DETAILS PACKER              |          1 |
| DETAILS PACKER              |          1 |
| DETAILS PACKER              |          1 |
| DETECTIVE VISION            |          1 |
| DETECTIVE VISION            |          1 |
| DETECTIVE VISION            |          1 |
| DEVIL DESIRE                |          1 |
| DEVIL DESIRE                |          1 |
| DIARY PANIC                 |          1 |
| DIARY PANIC                 |          1 |
| DINOSAUR SECRETARY          |          1 |
| DINOSAUR SECRETARY          |          1 |
| DINOSAUR SECRETARY          |          1 |
| DINOSAUR SECRETARY          |          1 |
| DIRTY ACE                   |          1 |
| DIRTY ACE                   |          1 |
| DIRTY ACE                   |          1 |
| DISCIPLE MOTHER             |          1 |
| DISCIPLE MOTHER             |          1 |
| DISCIPLE MOTHER             |          1 |
| DISCIPLE MOTHER             |          1 |
| DISTURBING SCARFACE         |          1 |
| DISTURBING SCARFACE         |          1 |
| DISTURBING SCARFACE         |          1 |
| DISTURBING SCARFACE         |          1 |
| DIVIDE MONSTER              |          1 |
| DIVIDE MONSTER              |          1 |
| DIVORCE SHINING             |          1 |
| DIVORCE SHINING             |          1 |
| DOCTOR GRAIL                |          1 |
| DOCTOR GRAIL                |          1 |
| DOGMA FAMILY                |          1 |
| DOGMA FAMILY                |          1 |
| DOGMA FAMILY                |          1 |
| DOGMA FAMILY                |          1 |
| DONNIE ALLEY                |          1 |
| DONNIE ALLEY                |          1 |
| DONNIE ALLEY                |          1 |
| DONNIE ALLEY                |          1 |
| DOOM DANCING                |          1 |
| DOOM DANCING                |          1 |
| DOORS PRESIDENT             |          1 |
| DOORS PRESIDENT             |          1 |
| DORADO NOTTING              |          1 |
| DORADO NOTTING              |          1 |
| DORADO NOTTING              |          1 |
| DORADO NOTTING              |          1 |
| DOUBLE WRATH                |          1 |
| DOUBLE WRATH                |          1 |
| DOUBLE WRATH                |          1 |
| DOWNHILL ENOUGH             |          1 |
| DOWNHILL ENOUGH             |          1 |
| DOWNHILL ENOUGH             |          1 |
| DRACULA CRYSTAL             |          1 |
| DRACULA CRYSTAL             |          1 |
| DRAGONFLY STRANGERS         |          1 |
| DRAGONFLY STRANGERS         |          1 |
| DREAM PICKUP                |          1 |
| DREAM PICKUP                |          1 |
| DREAM PICKUP                |          1 |
| DRIFTER COMMANDMENTS        |          1 |
| DRIFTER COMMANDMENTS        |          1 |
| DRIFTER COMMANDMENTS        |          1 |
| DRIFTER COMMANDMENTS        |          1 |
| DRIVER ANNIE                |          1 |
| DRIVER ANNIE                |          1 |
| DRIVING POLISH              |          1 |
| DRIVING POLISH              |          1 |
| DRIVING POLISH              |          1 |
| DRIVING POLISH              |          1 |
| DUCK RACER                  |          1 |
| DUCK RACER                  |          1 |
| DUFFEL APOCALYPSE           |          1 |
| DUFFEL APOCALYPSE           |          1 |
| DURHAM PANKY                |          1 |
| DURHAM PANKY                |          1 |
| DURHAM PANKY                |          1 |
| DURHAM PANKY                |          1 |
| DYING MAKER                 |          1 |
| DYING MAKER                 |          1 |
| DYING MAKER                 |          1 |
| DYING MAKER                 |          1 |
| DYNAMITE TARZAN             |          1 |
| DYNAMITE TARZAN             |          1 |
| DYNAMITE TARZAN             |          1 |
| DYNAMITE TARZAN             |          1 |
| EAGLES PANKY                |          1 |
| EAGLES PANKY                |          1 |
| EAGLES PANKY                |          1 |
| EAGLES PANKY                |          1 |
| EARRING INSTINCT            |          1 |
| EARRING INSTINCT            |          1 |
| EARTH VISION                |          1 |
| EARTH VISION                |          1 |
| EARTH VISION                |          1 |
| EASY GLADIATOR              |          1 |
| EASY GLADIATOR              |          1 |
| EASY GLADIATOR              |          1 |
| EDGE KISSING                |          1 |
| EDGE KISSING                |          1 |
| EDGE KISSING                |          1 |
| EDGE KISSING                |          1 |
| EFFECT GLADIATOR            |          1 |
| EFFECT GLADIATOR            |          1 |
| EFFECT GLADIATOR            |          1 |
| EFFECT GLADIATOR            |          1 |
| EGG IGBY                    |          1 |
| EGG IGBY                    |          1 |
| EGG IGBY                    |          1 |
| EGYPT TENENBAUMS            |          1 |
| EGYPT TENENBAUMS            |          1 |
| EGYPT TENENBAUMS            |          1 |
| ELEMENT FREDDY              |          1 |
| ELEMENT FREDDY              |          1 |
| ELEMENT FREDDY              |          1 |
| ELEMENT FREDDY              |          1 |
| ELEPHANT TROJAN             |          1 |
| ELEPHANT TROJAN             |          1 |
| ELEPHANT TROJAN             |          1 |
| ELF MURDER                  |          1 |
| ELF MURDER                  |          1 |
| ELIZABETH SHANE             |          1 |
| ELIZABETH SHANE             |          1 |
| EMPIRE MALKOVICH            |          1 |
| EMPIRE MALKOVICH            |          1 |
| EMPIRE MALKOVICH            |          1 |
| EMPIRE MALKOVICH            |          1 |
| ENCINO ELF                  |          1 |
| ENCINO ELF                  |          1 |
| ENCOUNTERS CURTAIN          |          1 |
| ENCOUNTERS CURTAIN          |          1 |
| ENCOUNTERS CURTAIN          |          1 |
| ENDING CROWDS               |          1 |
| ENDING CROWDS               |          1 |
| ENDING CROWDS               |          1 |
| ENEMY ODDS                  |          1 |
| ENEMY ODDS                  |          1 |
| ENEMY ODDS                  |          1 |
| ENGLISH BULWORTH            |          1 |
| ENGLISH BULWORTH            |          1 |
| ENGLISH BULWORTH            |          1 |
| ENOUGH RAGING               |          1 |
| ENOUGH RAGING               |          1 |
| ENTRAPMENT SATISFACTION     |          1 |
| ENTRAPMENT SATISFACTION     |          1 |
| ESCAPE METROPOLIS           |          1 |
| ESCAPE METROPOLIS           |          1 |
| EVE RESURRECTION            |          1 |
| EVE RESURRECTION            |          1 |
| EVERYONE CRAFT              |          1 |
| EVERYONE CRAFT              |          1 |
| EVERYONE CRAFT              |          1 |
| EVOLUTION ALTER             |          1 |
| EVOLUTION ALTER             |          1 |
| EVOLUTION ALTER             |          1 |
| EVOLUTION ALTER             |          1 |
| EXCITEMENT EVE              |          1 |
| EXCITEMENT EVE              |          1 |
| EXCITEMENT EVE              |          1 |
| EXORCIST STING              |          1 |
| EXORCIST STING              |          1 |
| EXPECATIONS NATURAL         |          1 |
| EXPECATIONS NATURAL         |          1 |
| EXPENDABLE STALLION         |          1 |
| EXPENDABLE STALLION         |          1 |
| EXPENDABLE STALLION         |          1 |
| EXPENDABLE STALLION         |          1 |
| EXPRESS LONELY              |          1 |
| EXPRESS LONELY              |          1 |
| EXPRESS LONELY              |          1 |
| EXPRESS LONELY              |          1 |
| EYES DRIVING                |          1 |
| EYES DRIVING                |          1 |
| FACTORY DRAGON              |          1 |
| FACTORY DRAGON              |          1 |
| FACTORY DRAGON              |          1 |
| FACTORY DRAGON              |          1 |
| FALCON VOLUME               |          1 |
| FALCON VOLUME               |          1 |
| FAMILY SWEET                |          1 |
| FAMILY SWEET                |          1 |
| FAMILY SWEET                |          1 |
| FAMILY SWEET                |          1 |
| FANTASIA PARK               |          1 |
| FANTASIA PARK               |          1 |
| FANTASY TROOPERS            |          1 |
| FANTASY TROOPERS            |          1 |
| FANTASY TROOPERS            |          1 |
| FANTASY TROOPERS            |          1 |
| FARGO GANDHI                |          1 |
| FARGO GANDHI                |          1 |
| FARGO GANDHI                |          1 |
| FARGO GANDHI                |          1 |
| FATAL HAUNTED               |          1 |
| FATAL HAUNTED               |          1 |
| FATAL HAUNTED               |          1 |
| FATAL HAUNTED               |          1 |
| FEATHERS METAL              |          1 |
| FEATHERS METAL              |          1 |
| FEATHERS METAL              |          1 |
| FELLOWSHIP AUTUMN           |          1 |
| FELLOWSHIP AUTUMN           |          1 |
| FELLOWSHIP AUTUMN           |          1 |
| FERRIS MOTHER               |          1 |
| FERRIS MOTHER               |          1 |
| FEUD FROGMEN                |          1 |
| FEUD FROGMEN                |          1 |
| FEVER EMPIRE                |          1 |
| FEVER EMPIRE                |          1 |
| FICTION CHRISTMAS           |          1 |
| FICTION CHRISTMAS           |          1 |
| FICTION CHRISTMAS           |          1 |
| FIDELITY DEVIL              |          1 |
| FIDELITY DEVIL              |          1 |
| FIDELITY DEVIL              |          1 |
| FIDELITY DEVIL              |          1 |
| FIGHT JAWBREAKER            |          1 |
| FIGHT JAWBREAKER            |          1 |
| FIREBALL PHILADELPHIA       |          1 |
| FIREBALL PHILADELPHIA       |          1 |
| FIREBALL PHILADELPHIA       |          1 |
| FIREBALL PHILADELPHIA       |          1 |
| FISH OPUS                   |          1 |
| FISH OPUS                   |          1 |
| FISH OPUS                   |          1 |
| FLAMINGOS CONNECTICUT       |          1 |
| FLAMINGOS CONNECTICUT       |          1 |
| FLAMINGOS CONNECTICUT       |          1 |
| FLASH WARS                  |          1 |
| FLASH WARS                  |          1 |
| FLASH WARS                  |          1 |
| FLASH WARS                  |          1 |
| FLATLINERS KILLER           |          1 |
| FLATLINERS KILLER           |          1 |
| FLATLINERS KILLER           |          1 |
| FLATLINERS KILLER           |          1 |
| FLINTSTONES HAPPINESS       |          1 |
| FLINTSTONES HAPPINESS       |          1 |
| FLINTSTONES HAPPINESS       |          1 |
| FLYING HOOK                 |          1 |
| FLYING HOOK                 |          1 |
| FOOL MOCKINGBIRD            |          1 |
| FOOL MOCKINGBIRD            |          1 |
| FOOL MOCKINGBIRD            |          1 |
| FOOL MOCKINGBIRD            |          1 |
| FORREST SONS                |          1 |
| FORREST SONS                |          1 |
| FORREST SONS                |          1 |
| FORRESTER COMANCHEROS       |          1 |
| FORRESTER COMANCHEROS       |          1 |
| FORRESTER COMANCHEROS       |          1 |
| FORRESTER COMANCHEROS       |          1 |
| FORWARD TEMPLE              |          1 |
| FORWARD TEMPLE              |          1 |
| FORWARD TEMPLE              |          1 |
| FORWARD TEMPLE              |          1 |
| FREAKY POCUS                |          1 |
| FREAKY POCUS                |          1 |
| FREDDY STORM                |          1 |
| FREDDY STORM                |          1 |
| FREEDOM CLEOPATRA           |          1 |
| FREEDOM CLEOPATRA           |          1 |
| FRENCH HOLIDAY              |          1 |
| FRENCH HOLIDAY              |          1 |
| FRENCH HOLIDAY              |          1 |
| FRIDA SLIPPER               |          1 |
| FRIDA SLIPPER               |          1 |
| FRONTIER CABIN              |          1 |
| FRONTIER CABIN              |          1 |
| FROST HEAD                  |          1 |
| FROST HEAD                  |          1 |
| FROST HEAD                  |          1 |
| FROST HEAD                  |          1 |
| FUGITIVE MAGUIRE            |          1 |
| FUGITIVE MAGUIRE            |          1 |
| FUGITIVE MAGUIRE            |          1 |
| FUGITIVE MAGUIRE            |          1 |
| FULL FLATLINERS             |          1 |
| FULL FLATLINERS             |          1 |
| FURY MURDER                 |          1 |
| FURY MURDER                 |          1 |
| FURY MURDER                 |          1 |
| GABLES METROPOLIS           |          1 |
| GABLES METROPOLIS           |          1 |
| GABLES METROPOLIS           |          1 |
| GALAXY SWEETHEARTS          |          1 |
| GALAXY SWEETHEARTS          |          1 |
| GAMES BOWFINGER             |          1 |
| GAMES BOWFINGER             |          1 |
| GAMES BOWFINGER             |          1 |
| GAMES BOWFINGER             |          1 |
| GANGS PRIDE                 |          1 |
| GANGS PRIDE                 |          1 |
| GANGS PRIDE                 |          1 |
| GANGS PRIDE                 |          1 |
| GARDEN ISLAND               |          1 |
| GARDEN ISLAND               |          1 |
| GARDEN ISLAND               |          1 |
| GARDEN ISLAND               |          1 |
| GASLIGHT CRUSADE            |          1 |
| GASLIGHT CRUSADE            |          1 |
| GASLIGHT CRUSADE            |          1 |
| GENTLEMEN STAGE             |          1 |
| GENTLEMEN STAGE             |          1 |
| GHOST GROUNDHOG             |          1 |
| GHOST GROUNDHOG             |          1 |
| GHOST GROUNDHOG             |          1 |
| GIANT TROOPERS              |          1 |
| GIANT TROOPERS              |          1 |
| GIANT TROOPERS              |          1 |
| GIANT TROOPERS              |          1 |
| GILMORE BOILED              |          1 |
| GILMORE BOILED              |          1 |
| GILMORE BOILED              |          1 |
| GILMORE BOILED              |          1 |
| GLASS DYING                 |          1 |
| GLASS DYING                 |          1 |
| GLASS DYING                 |          1 |
| GLASS DYING                 |          1 |
| GLEAMING JAWBREAKER         |          1 |
| GLEAMING JAWBREAKER         |          1 |
| GLEAMING JAWBREAKER         |          1 |
| GLEAMING JAWBREAKER         |          1 |
| GLORY TRACY                 |          1 |
| GLORY TRACY                 |          1 |
| GO PURPLE                   |          1 |
| GO PURPLE                   |          1 |
| GO PURPLE                   |          1 |
| GODFATHER DIARY             |          1 |
| GODFATHER DIARY             |          1 |
| GODFATHER DIARY             |          1 |
| GOLD RIVER                  |          1 |
| GOLD RIVER                  |          1 |
| GOLDFINGER SENSIBILITY      |          1 |
| GOLDFINGER SENSIBILITY      |          1 |
| GOLDFINGER SENSIBILITY      |          1 |
| GOLDFINGER SENSIBILITY      |          1 |
| GOLDMINE TYCOON             |          1 |
| GOLDMINE TYCOON             |          1 |
| GOLDMINE TYCOON             |          1 |
| GOLDMINE TYCOON             |          1 |
| GONE TROUBLE                |          1 |
| GONE TROUBLE                |          1 |
| GOODFELLAS SALUTE           |          1 |
| GOODFELLAS SALUTE           |          1 |
| GOODFELLAS SALUTE           |          1 |
| GOODFELLAS SALUTE           |          1 |
| GORGEOUS BINGO              |          1 |
| GORGEOUS BINGO              |          1 |
| GORGEOUS BINGO              |          1 |
| GOSFORD DONNIE              |          1 |
| GOSFORD DONNIE              |          1 |
| GOSFORD DONNIE              |          1 |
| GRACELAND DYNAMITE          |          1 |
| GRACELAND DYNAMITE          |          1 |
| GRADUATE LORD               |          1 |
| GRADUATE LORD               |          1 |
| GRADUATE LORD               |          1 |
| GRAFFITI LOVE               |          1 |
| GRAFFITI LOVE               |          1 |
| GRAFFITI LOVE               |          1 |
| GRAIL FRANKENSTEIN          |          1 |
| GRAIL FRANKENSTEIN          |          1 |
| GRAPES FURY                 |          1 |
| GRAPES FURY                 |          1 |
| GRAPES FURY                 |          1 |
| GRAPES FURY                 |          1 |
| GREASE YOUTH                |          1 |
| GREASE YOUTH                |          1 |
| GREASE YOUTH                |          1 |
| GREATEST NORTH              |          1 |
| GREATEST NORTH              |          1 |
| GREATEST NORTH              |          1 |
| GREATEST NORTH              |          1 |
| GREEK EVERYONE              |          1 |
| GREEK EVERYONE              |          1 |
| GRINCH MASSAGE              |          1 |
| GRINCH MASSAGE              |          1 |
| GRIT CLOCKWORK              |          1 |
| GRIT CLOCKWORK              |          1 |
| GRIT CLOCKWORK              |          1 |
| GRIT CLOCKWORK              |          1 |
| GROOVE FICTION              |          1 |
| GROOVE FICTION              |          1 |
| GROOVE FICTION              |          1 |
| GROUNDHOG UNCUT             |          1 |
| GROUNDHOG UNCUT             |          1 |
| GUN BONNIE                  |          1 |
| GUN BONNIE                  |          1 |
| GUN BONNIE                  |          1 |
| GUNFIGHT MOON               |          1 |
| GUNFIGHT MOON               |          1 |
| GUNFIGHT MOON               |          1 |
| GUNFIGHTER MUSSOLINI        |          1 |
| GUNFIGHTER MUSSOLINI        |          1 |
| GUYS FALCON                 |          1 |
| GUYS FALCON                 |          1 |
| GUYS FALCON                 |          1 |
| HALF OUTFIELD               |          1 |
| HALF OUTFIELD               |          1 |
| HALF OUTFIELD               |          1 |
| HALF OUTFIELD               |          1 |
| HALL CASSIDY                |          1 |
| HALL CASSIDY                |          1 |
| HALL CASSIDY                |          1 |
| HALL CASSIDY                |          1 |
| HALLOWEEN NUTS              |          1 |
| HALLOWEEN NUTS              |          1 |
| HAMLET WISDOM               |          1 |
| HAMLET WISDOM               |          1 |
| HAMLET WISDOM               |          1 |
| HAMLET WISDOM               |          1 |
| HANDICAP BOONDOCK           |          1 |
| HANDICAP BOONDOCK           |          1 |
| HANDICAP BOONDOCK           |          1 |
| HANKY OCTOBER               |          1 |
| HANKY OCTOBER               |          1 |
| HANKY OCTOBER               |          1 |
| HARDLY ROBBERS              |          1 |
| HARDLY ROBBERS              |          1 |
| HAROLD FRENCH               |          1 |
| HAROLD FRENCH               |          1 |
| HARPER DYING                |          1 |
| HARPER DYING                |          1 |
| HARPER DYING                |          1 |
| HARRY IDAHO                 |          1 |
| HARRY IDAHO                 |          1 |
| HARRY IDAHO                 |          1 |
| HARRY IDAHO                 |          1 |
| HAUNTING PIANIST            |          1 |
| HAUNTING PIANIST            |          1 |
| HAWK CHILL                  |          1 |
| HAWK CHILL                  |          1 |
| HEAD STRANGER               |          1 |
| HEAD STRANGER               |          1 |
| HEAD STRANGER               |          1 |
| HEAD STRANGER               |          1 |
| HEARTBREAKERS BRIGHT        |          1 |
| HEARTBREAKERS BRIGHT        |          1 |
| HEARTBREAKERS BRIGHT        |          1 |
| HEARTBREAKERS BRIGHT        |          1 |
| HEAVEN FREEDOM              |          1 |
| HEAVEN FREEDOM              |          1 |
| HEAVEN FREEDOM              |          1 |
| HEAVENLY GUN                |          1 |
| HEAVENLY GUN                |          1 |
| HEAVYWEIGHTS BEAST          |          1 |
| HEAVYWEIGHTS BEAST          |          1 |
| HEAVYWEIGHTS BEAST          |          1 |
| HEAVYWEIGHTS BEAST          |          1 |
| HEDWIG ALTER                |          1 |
| HEDWIG ALTER                |          1 |
| HEDWIG ALTER                |          1 |
| HELLFIGHTERS SIERRA         |          1 |
| HELLFIGHTERS SIERRA         |          1 |
| HELLFIGHTERS SIERRA         |          1 |
| HIGH ENCINO                 |          1 |
| HIGH ENCINO                 |          1 |
| HIGH ENCINO                 |          1 |
| HIGHBALL POTTER             |          1 |
| HIGHBALL POTTER             |          1 |
| HILLS NEIGHBORS             |          1 |
| HILLS NEIGHBORS             |          1 |
| HILLS NEIGHBORS             |          1 |
| HILLS NEIGHBORS             |          1 |
| HOBBIT ALIEN                |          1 |
| HOBBIT ALIEN                |          1 |
| HOBBIT ALIEN                |          1 |
| HOBBIT ALIEN                |          1 |
| HOLES BRANNIGAN             |          1 |
| HOLES BRANNIGAN             |          1 |
| HOLLYWOOD ANONYMOUS         |          1 |
| HOLLYWOOD ANONYMOUS         |          1 |
| HOLOCAUST HIGHBALL          |          1 |
| HOLOCAUST HIGHBALL          |          1 |
| HOLOCAUST HIGHBALL          |          1 |
| HOMEWARD CIDER              |          1 |
| HOMEWARD CIDER              |          1 |
| HOMEWARD CIDER              |          1 |
| HOMEWARD CIDER              |          1 |
| HOMICIDE PEACH              |          1 |
| HOMICIDE PEACH              |          1 |
| HOMICIDE PEACH              |          1 |
| HOMICIDE PEACH              |          1 |
| HONEY TIES                  |          1 |
| HONEY TIES                  |          1 |
| HOPE TOOTSIE                |          1 |
| HOPE TOOTSIE                |          1 |
| HOPE TOOTSIE                |          1 |
| HORN WORKING                |          1 |
| HORN WORKING                |          1 |
| HORN WORKING                |          1 |
| HORN WORKING                |          1 |
| HORROR REIGN                |          1 |
| HORROR REIGN                |          1 |
| HORROR REIGN                |          1 |
| HORROR REIGN                |          1 |
| HOTEL HAPPINESS             |          1 |
| HOTEL HAPPINESS             |          1 |
| HOURS RAGE                  |          1 |
| HOURS RAGE                  |          1 |
| HOURS RAGE                  |          1 |
| HOUSE DYNAMITE              |          1 |
| HOUSE DYNAMITE              |          1 |
| HUMAN GRAFFITI              |          1 |
| HUMAN GRAFFITI              |          1 |
| HUNCHBACK IMPOSSIBLE        |          1 |
| HUNCHBACK IMPOSSIBLE        |          1 |
| HUNCHBACK IMPOSSIBLE        |          1 |
| HUNCHBACK IMPOSSIBLE        |          1 |
| HUNGER ROOF                 |          1 |
| HUNGER ROOF                 |          1 |
| HUNTER ALTER                |          1 |
| HUNTER ALTER                |          1 |
| HUNTING MUSKETEERS          |          1 |
| HUNTING MUSKETEERS          |          1 |
| HUNTING MUSKETEERS          |          1 |
| HURRICANE AFFAIR            |          1 |
| HURRICANE AFFAIR            |          1 |
| HURRICANE AFFAIR            |          1 |
| HUSTLER PARTY               |          1 |
| HUSTLER PARTY               |          1 |
| HUSTLER PARTY               |          1 |
| HUSTLER PARTY               |          1 |
| HYDE DOCTOR                 |          1 |
| HYDE DOCTOR                 |          1 |
| HYDE DOCTOR                 |          1 |
| HYSTERICAL GRAIL            |          1 |
| HYSTERICAL GRAIL            |          1 |
| ICE CROSSING                |          1 |
| ICE CROSSING                |          1 |
| ICE CROSSING                |          1 |
| ICE CROSSING                |          1 |
| IDAHO LOVE                  |          1 |
| IDAHO LOVE                  |          1 |
| IDOLS SNATCHERS             |          1 |
| IDOLS SNATCHERS             |          1 |
| IDOLS SNATCHERS             |          1 |
| IGBY MAKER                  |          1 |
| IGBY MAKER                  |          1 |
| IMAGE PRINCESS              |          1 |
| IMAGE PRINCESS              |          1 |
| IMAGE PRINCESS              |          1 |
| IMPACT ALADDIN              |          1 |
| IMPACT ALADDIN              |          1 |
| IMPOSSIBLE PREJUDICE        |          1 |
| IMPOSSIBLE PREJUDICE        |          1 |
| IMPOSSIBLE PREJUDICE        |          1 |
| IMPOSSIBLE PREJUDICE        |          1 |
| INCH JET                    |          1 |
| INCH JET                    |          1 |
| INDEPENDENCE HOTEL          |          1 |
| INDEPENDENCE HOTEL          |          1 |
| INDIAN LOVE                 |          1 |
| INDIAN LOVE                 |          1 |
| INNOCENT USUAL              |          1 |
| INNOCENT USUAL              |          1 |
| INNOCENT USUAL              |          1 |
| INNOCENT USUAL              |          1 |
| INSECTS STONE               |          1 |
| INSECTS STONE               |          1 |
| INSIDER ARIZONA             |          1 |
| INSIDER ARIZONA             |          1 |
| INSTINCT AIRPORT            |          1 |
| INSTINCT AIRPORT            |          1 |
| INSTINCT AIRPORT            |          1 |
| INTENTIONS EMPIRE           |          1 |
| INTENTIONS EMPIRE           |          1 |
| INTENTIONS EMPIRE           |          1 |
| INTENTIONS EMPIRE           |          1 |
| INTERVIEW LIAISONS          |          1 |
| INTERVIEW LIAISONS          |          1 |
| INTOLERABLE INTENTIONS      |          1 |
| INTOLERABLE INTENTIONS      |          1 |
| INTRIGUE WORST              |          1 |
| INTRIGUE WORST              |          1 |
| INTRIGUE WORST              |          1 |
| INTRIGUE WORST              |          1 |
| INVASION CYCLONE            |          1 |
| INVASION CYCLONE            |          1 |
| INVASION CYCLONE            |          1 |
| INVASION CYCLONE            |          1 |
| ISHTAR ROCKETEER            |          1 |
| ISHTAR ROCKETEER            |          1 |
| ISLAND EXORCIST             |          1 |
| ISLAND EXORCIST             |          1 |
| ISLAND EXORCIST             |          1 |
| JACKET FRISCO               |          1 |
| JACKET FRISCO               |          1 |
| JASON TRAP                  |          1 |
| JASON TRAP                  |          1 |
| JASON TRAP                  |          1 |
| JAWS HARRY                  |          1 |
| JAWS HARRY                  |          1 |
| JEDI BENEATH                |          1 |
| JEDI BENEATH                |          1 |
| JEEPERS WEDDING             |          1 |
| JEEPERS WEDDING             |          1 |
| JEKYLL FROGMEN              |          1 |
| JEKYLL FROGMEN              |          1 |
| JEKYLL FROGMEN              |          1 |
| JEOPARDY ENCINO             |          1 |
| JEOPARDY ENCINO             |          1 |
| JEOPARDY ENCINO             |          1 |
| JERICHO MULAN               |          1 |
| JERICHO MULAN               |          1 |
| JERICHO MULAN               |          1 |
| JERK PAYCHECK               |          1 |
| JERK PAYCHECK               |          1 |
| JERK PAYCHECK               |          1 |
| JERK PAYCHECK               |          1 |
| JET NEIGHBORS               |          1 |
| JET NEIGHBORS               |          1 |
| JET NEIGHBORS               |          1 |
| JET NEIGHBORS               |          1 |
| JOON NORTHWEST              |          1 |
| JOON NORTHWEST              |          1 |
| JUGGLER HARDLY              |          1 |
| JUGGLER HARDLY              |          1 |
| JUGGLER HARDLY              |          1 |
| JUGGLER HARDLY              |          1 |
| JUMANJI BLADE               |          1 |
| JUMANJI BLADE               |          1 |
| JUMPING WRATH               |          1 |
| JUMPING WRATH               |          1 |
| JUNGLE CLOSER               |          1 |
| JUNGLE CLOSER               |          1 |
| KARATE MOON                 |          1 |
| KARATE MOON                 |          1 |
| KARATE MOON                 |          1 |
| KARATE MOON                 |          1 |
| KICK SAVANNAH               |          1 |
| KICK SAVANNAH               |          1 |
| KILLER INNOCENT             |          1 |
| KILLER INNOCENT             |          1 |
| KING EVOLUTION              |          1 |
| KING EVOLUTION              |          1 |
| KISS GLORY                  |          1 |
| KISS GLORY                  |          1 |
| KISS GLORY                  |          1 |
| KISS GLORY                  |          1 |
| KISSING DOLLS               |          1 |
| KISSING DOLLS               |          1 |
| KISSING DOLLS               |          1 |
| KNOCK WARLOCK               |          1 |
| KNOCK WARLOCK               |          1 |
| KNOCK WARLOCK               |          1 |
| KNOCK WARLOCK               |          1 |
| KRAMER CHOCOLATE            |          1 |
| KRAMER CHOCOLATE            |          1 |
| KRAMER CHOCOLATE            |          1 |
| KWAI HOMEWARD               |          1 |
| KWAI HOMEWARD               |          1 |
| KWAI HOMEWARD               |          1 |
| KWAI HOMEWARD               |          1 |
| LADY STAGE                  |          1 |
| LADY STAGE                  |          1 |
| LADY STAGE                  |          1 |
| LADY STAGE                  |          1 |
| LAWLESS VISION              |          1 |
| LAWLESS VISION              |          1 |
| LAWLESS VISION              |          1 |
| LAWLESS VISION              |          1 |
| LAWRENCE LOVE               |          1 |
| LAWRENCE LOVE               |          1 |
| LEAGUE HELLFIGHTERS         |          1 |
| LEAGUE HELLFIGHTERS         |          1 |
| LEBOWSKI SOLDIERS           |          1 |
| LEBOWSKI SOLDIERS           |          1 |
| LIAISONS SWEET              |          1 |
| LIAISONS SWEET              |          1 |
| LICENSE WEEKEND             |          1 |
| LICENSE WEEKEND             |          1 |
| LIES TREATMENT              |          1 |
| LIES TREATMENT              |          1 |
| LIES TREATMENT              |          1 |
| LIES TREATMENT              |          1 |
| LIGHTS DEER                 |          1 |
| LIGHTS DEER                 |          1 |
| LION UNCUT                  |          1 |
| LION UNCUT                  |          1 |
| LOATHING LEGALLY            |          1 |
| LOATHING LEGALLY            |          1 |
| LOATHING LEGALLY            |          1 |
| LOATHING LEGALLY            |          1 |
| LOLA AGENT                  |          1 |
| LOLA AGENT                  |          1 |
| LOLITA WORLD                |          1 |
| LOLITA WORLD                |          1 |
| LOLITA WORLD                |          1 |
| LONELY ELEPHANT             |          1 |
| LONELY ELEPHANT             |          1 |
| LONELY ELEPHANT             |          1 |
| LONELY ELEPHANT             |          1 |
| LORD ARIZONA                |          1 |
| LORD ARIZONA                |          1 |
| LORD ARIZONA                |          1 |
| LOSE INCH                   |          1 |
| LOSE INCH                   |          1 |
| LOSE INCH                   |          1 |
| LOSE INCH                   |          1 |
| LOST BIRD                   |          1 |
| LOST BIRD                   |          1 |
| LOST BIRD                   |          1 |
| LOUISIANA HARRY             |          1 |
| LOUISIANA HARRY             |          1 |
| LOVE SUICIDES               |          1 |
| LOVE SUICIDES               |          1 |
| LOVE SUICIDES               |          1 |
| LOVE SUICIDES               |          1 |
| LOVELY JINGLE               |          1 |
| LOVELY JINGLE               |          1 |
| LOVELY JINGLE               |          1 |
| LUCK OPUS                   |          1 |
| LUCK OPUS                   |          1 |
| LUCKY FLYING                |          1 |
| LUCKY FLYING                |          1 |
| LUCKY FLYING                |          1 |
| LUST LOCK                   |          1 |
| LUST LOCK                   |          1 |
| LUST LOCK                   |          1 |
| LUST LOCK                   |          1 |
| MADIGAN DORADO              |          1 |
| MADIGAN DORADO              |          1 |
| MADISON TRAP                |          1 |
| MADISON TRAP                |          1 |
| MADNESS ATTACKS             |          1 |
| MADNESS ATTACKS             |          1 |
| MADNESS ATTACKS             |          1 |
| MADNESS ATTACKS             |          1 |
| MAGNIFICENT CHITTY          |          1 |
| MAGNIFICENT CHITTY          |          1 |
| MAGNOLIA FORRESTER          |          1 |
| MAGNOLIA FORRESTER          |          1 |
| MAGUIRE APACHE              |          1 |
| MAGUIRE APACHE              |          1 |
| MAGUIRE APACHE              |          1 |
| MAIDEN HOME                 |          1 |
| MAIDEN HOME                 |          1 |
| MAIDEN HOME                 |          1 |
| MALKOVICH PET               |          1 |
| MALKOVICH PET               |          1 |
| MALKOVICH PET               |          1 |
| MALKOVICH PET               |          1 |
| MALLRATS UNITED             |          1 |
| MALLRATS UNITED             |          1 |
| MALLRATS UNITED             |          1 |
| MALTESE HOPE                |          1 |
| MALTESE HOPE                |          1 |
| MALTESE HOPE                |          1 |
| MANCHURIAN CURTAIN          |          1 |
| MANCHURIAN CURTAIN          |          1 |
| MARRIED GO                  |          1 |
| MARRIED GO                  |          1 |
| MARRIED GO                  |          1 |
| MARRIED GO                  |          1 |
| MARS ROMAN                  |          1 |
| MARS ROMAN                  |          1 |
| MARS ROMAN                  |          1 |
| MASK PEACH                  |          1 |
| MASK PEACH                  |          1 |
| MASK PEACH                  |          1 |
| MASK PEACH                  |          1 |
| MASKED BUBBLE               |          1 |
| MASKED BUBBLE               |          1 |
| MASKED BUBBLE               |          1 |
| MASKED BUBBLE               |          1 |
| MASSACRE USUAL              |          1 |
| MASSACRE USUAL              |          1 |
| MASSACRE USUAL              |          1 |
| MASSACRE USUAL              |          1 |
| MATRIX SNOWMAN              |          1 |
| MATRIX SNOWMAN              |          1 |
| MAUDE MOD                   |          1 |
| MAUDE MOD                   |          1 |
| MEET CHOCOLATE              |          1 |
| MEET CHOCOLATE              |          1 |
| MEMENTO ZOOLANDER           |          1 |
| MEMENTO ZOOLANDER           |          1 |
| MENAGERIE RUSHMORE          |          1 |
| MENAGERIE RUSHMORE          |          1 |
| MERMAID INSECTS             |          1 |
| MERMAID INSECTS             |          1 |
| METAL ARMAGEDDON            |          1 |
| METAL ARMAGEDDON            |          1 |
| METROPOLIS COMA             |          1 |
| METROPOLIS COMA             |          1 |
| METROPOLIS COMA             |          1 |
| METROPOLIS COMA             |          1 |
| MICROCOSMOS PARADISE        |          1 |
| MICROCOSMOS PARADISE        |          1 |
| MICROCOSMOS PARADISE        |          1 |
| MICROCOSMOS PARADISE        |          1 |
| MIDNIGHT WESTWARD           |          1 |
| MIDNIGHT WESTWARD           |          1 |
| MIDSUMMER GROUNDHOG         |          1 |
| MIDSUMMER GROUNDHOG         |          1 |
| MILE MULAN                  |          1 |
| MILE MULAN                  |          1 |
| MILE MULAN                  |          1 |
| MILLION ACE                 |          1 |
| MILLION ACE                 |          1 |
| MINDS TRUMAN                |          1 |
| MINDS TRUMAN                |          1 |
| MINDS TRUMAN                |          1 |
| MINDS TRUMAN                |          1 |
| MINE TITANS                 |          1 |
| MINE TITANS                 |          1 |
| MINE TITANS                 |          1 |
| MINE TITANS                 |          1 |
| MINORITY KISS               |          1 |
| MINORITY KISS               |          1 |
| MINORITY KISS               |          1 |
| MISSION ZOOLANDER           |          1 |
| MISSION ZOOLANDER           |          1 |
| MISSION ZOOLANDER           |          1 |
| MIXED DOORS                 |          1 |
| MIXED DOORS                 |          1 |
| MOCKINGBIRD HOLLYWOOD       |          1 |
| MOCKINGBIRD HOLLYWOOD       |          1 |
| MOCKINGBIRD HOLLYWOOD       |          1 |
| MOCKINGBIRD HOLLYWOOD       |          1 |
| MOD SECRETARY               |          1 |
| MOD SECRETARY               |          1 |
| MOD SECRETARY               |          1 |
| MONEY HAROLD                |          1 |
| MONEY HAROLD                |          1 |
| MONEY HAROLD                |          1 |
| MONSTER SPARTACUS           |          1 |
| MONSTER SPARTACUS           |          1 |
| MONTEZUMA COMMAND           |          1 |
| MONTEZUMA COMMAND           |          1 |
| MONTEZUMA COMMAND           |          1 |
| MOON BUNCH                  |          1 |
| MOON BUNCH                  |          1 |
| MOON BUNCH                  |          1 |
| MOON BUNCH                  |          1 |
| MOONSHINE CABIN             |          1 |
| MOONSHINE CABIN             |          1 |
| MOSQUITO ARMAGEDDON         |          1 |
| MOSQUITO ARMAGEDDON         |          1 |
| MOSQUITO ARMAGEDDON         |          1 |
| MOSQUITO ARMAGEDDON         |          1 |
| MOTHER OLEANDER             |          1 |
| MOTHER OLEANDER             |          1 |
| MOTHER OLEANDER             |          1 |
| MOTIONS DETAILS             |          1 |
| MOTIONS DETAILS             |          1 |
| MOULIN WAKE                 |          1 |
| MOULIN WAKE                 |          1 |
| MOULIN WAKE                 |          1 |
| MOURNING PURPLE             |          1 |
| MOURNING PURPLE             |          1 |
| MOVIE SHAKESPEARE           |          1 |
| MOVIE SHAKESPEARE           |          1 |
| MOVIE SHAKESPEARE           |          1 |
| MOVIE SHAKESPEARE           |          1 |
| MUMMY CREATURES             |          1 |
| MUMMY CREATURES             |          1 |
| MURDER ANTITRUST            |          1 |
| MURDER ANTITRUST            |          1 |
| MUSCLE BRIGHT               |          1 |
| MUSCLE BRIGHT               |          1 |
| MUSCLE BRIGHT               |          1 |
| MUSCLE BRIGHT               |          1 |
| MUSIC BOONDOCK              |          1 |
| MUSIC BOONDOCK              |          1 |
| MUSKETEERS WAIT             |          1 |
| MUSKETEERS WAIT             |          1 |
| MUSKETEERS WAIT             |          1 |
| MUSKETEERS WAIT             |          1 |
| MYSTIC TRUMAN               |          1 |
| MYSTIC TRUMAN               |          1 |
| NAME DETECTIVE              |          1 |
| NAME DETECTIVE              |          1 |
| NAME DETECTIVE              |          1 |
| NATIONAL STORY              |          1 |
| NATIONAL STORY              |          1 |
| NATURAL STOCK               |          1 |
| NATURAL STOCK               |          1 |
| NATURAL STOCK               |          1 |
| NEIGHBORS CHARADE           |          1 |
| NEIGHBORS CHARADE           |          1 |
| NEMO CAMPUS                 |          1 |
| NEMO CAMPUS                 |          1 |
| NETWORK PEAK                |          1 |
| NETWORK PEAK                |          1 |
| NETWORK PEAK                |          1 |
| NETWORK PEAK                |          1 |
| NEWTON LABYRINTH            |          1 |
| NEWTON LABYRINTH            |          1 |
| NIGHTMARE CHILL             |          1 |
| NIGHTMARE CHILL             |          1 |
| NIGHTMARE CHILL             |          1 |
| NONE SPIKING                |          1 |
| NONE SPIKING                |          1 |
| NONE SPIKING                |          1 |
| NORTHWEST POLISH            |          1 |
| NORTHWEST POLISH            |          1 |
| NORTHWEST POLISH            |          1 |
| NOVOCAINE FLIGHT            |          1 |
| NOVOCAINE FLIGHT            |          1 |
| NOVOCAINE FLIGHT            |          1 |
| NUTS TIES                   |          1 |
| NUTS TIES                   |          1 |
| NUTS TIES                   |          1 |
| OLEANDER CLUE               |          1 |
| OLEANDER CLUE               |          1 |
| OLEANDER CLUE               |          1 |
| OPEN AFRICAN                |          1 |
| OPEN AFRICAN                |          1 |
| OPERATION OPERATION         |          1 |
| OPERATION OPERATION         |          1 |
| OPERATION OPERATION         |          1 |
| OPERATION OPERATION         |          1 |
| ORANGE GRAPES               |          1 |
| ORANGE GRAPES               |          1 |
| ORANGE GRAPES               |          1 |
| ORIENT CLOSER               |          1 |
| ORIENT CLOSER               |          1 |
| ORIENT CLOSER               |          1 |
| OSCAR GOLD                  |          1 |
| OSCAR GOLD                  |          1 |
| OSCAR GOLD                  |          1 |
| OTHERS SOUP                 |          1 |
| OTHERS SOUP                 |          1 |
| OTHERS SOUP                 |          1 |
| OUTBREAK DIVINE             |          1 |
| OUTBREAK DIVINE             |          1 |
| OUTBREAK DIVINE             |          1 |
| OUTFIELD MASSACRE           |          1 |
| OUTFIELD MASSACRE           |          1 |
| OUTFIELD MASSACRE           |          1 |
| OUTLAW HANKY                |          1 |
| OUTLAW HANKY                |          1 |
| OUTLAW HANKY                |          1 |
| OUTLAW HANKY                |          1 |
| OZ LIAISONS                 |          1 |
| OZ LIAISONS                 |          1 |
| PACIFIC AMISTAD             |          1 |
| PACIFIC AMISTAD             |          1 |
| PACKER MADIGAN              |          1 |
| PACKER MADIGAN              |          1 |
| PAJAMA JAWBREAKER           |          1 |
| PAJAMA JAWBREAKER           |          1 |
| PAJAMA JAWBREAKER           |          1 |
| PAJAMA JAWBREAKER           |          1 |
| PANIC CLUB                  |          1 |
| PANIC CLUB                  |          1 |
| PANKY SUBMARINE             |          1 |
| PANKY SUBMARINE             |          1 |
| PANTHER REDS                |          1 |
| PANTHER REDS                |          1 |
| PANTHER REDS                |          1 |
| PARADISE SABRINA            |          1 |
| PARADISE SABRINA            |          1 |
| PARADISE SABRINA            |          1 |
| PARADISE SABRINA            |          1 |
| PARTY KNOCK                 |          1 |
| PARTY KNOCK                 |          1 |
| PAST SUICIDES               |          1 |
| PAST SUICIDES               |          1 |
| PAST SUICIDES               |          1 |
| PAST SUICIDES               |          1 |
| PATHS CONTROL               |          1 |
| PATHS CONTROL               |          1 |
| PATIENT SISTER              |          1 |
| PATIENT SISTER              |          1 |
| PATIENT SISTER              |          1 |
| PATRIOT ROMAN               |          1 |
| PATRIOT ROMAN               |          1 |
| PATTON INTERVIEW            |          1 |
| PATTON INTERVIEW            |          1 |
| PATTON INTERVIEW            |          1 |
| PATTON INTERVIEW            |          1 |
| PAYCHECK WAIT               |          1 |
| PAYCHECK WAIT               |          1 |
| PAYCHECK WAIT               |          1 |
| PEACH INNOCENT              |          1 |
| PEACH INNOCENT              |          1 |
| PEAK FOREVER                |          1 |
| PEAK FOREVER                |          1 |
| PELICAN COMFORTS            |          1 |
| PELICAN COMFORTS            |          1 |
| PELICAN COMFORTS            |          1 |
| PELICAN COMFORTS            |          1 |
| PERFECT GROOVE              |          1 |
| PERFECT GROOVE              |          1 |
| PERSONAL LADYBUGS           |          1 |
| PERSONAL LADYBUGS           |          1 |
| PET HAUNTING                |          1 |
| PET HAUNTING                |          1 |
| PET HAUNTING                |          1 |
| PHANTOM GLORY               |          1 |
| PHANTOM GLORY               |          1 |
| PHILADELPHIA WIFE           |          1 |
| PHILADELPHIA WIFE           |          1 |
| PIANIST OUTFIELD            |          1 |
| PIANIST OUTFIELD            |          1 |
| PIANIST OUTFIELD            |          1 |
| PICKUP DRIVING              |          1 |
| PICKUP DRIVING              |          1 |
| PICKUP DRIVING              |          1 |
| PICKUP DRIVING              |          1 |
| PILOT HOOSIERS              |          1 |
| PILOT HOOSIERS              |          1 |
| PINOCCHIO SIMON             |          1 |
| PINOCCHIO SIMON             |          1 |
| PIRATES ROXANNE             |          1 |
| PIRATES ROXANNE             |          1 |
| PIRATES ROXANNE             |          1 |
| PITTSBURGH HUNCHBACK        |          1 |
| PITTSBURGH HUNCHBACK        |          1 |
| PITTSBURGH HUNCHBACK        |          1 |
| PITY BOUND                  |          1 |
| PITY BOUND                  |          1 |
| PITY BOUND                  |          1 |
| PITY BOUND                  |          1 |
| PLUTO OLEANDER              |          1 |
| PLUTO OLEANDER              |          1 |
| PLUTO OLEANDER              |          1 |
| PLUTO OLEANDER              |          1 |
| POCUS PULP                  |          1 |
| POCUS PULP                  |          1 |
| POCUS PULP                  |          1 |
| POLLOCK DELIVERANCE         |          1 |
| POLLOCK DELIVERANCE         |          1 |
| POLLOCK DELIVERANCE         |          1 |
| POLLOCK DELIVERANCE         |          1 |
| POND SEATTLE                |          1 |
| POND SEATTLE                |          1 |
| POND SEATTLE                |          1 |
| POND SEATTLE                |          1 |
| POSEIDON FOREVER            |          1 |
| POSEIDON FOREVER            |          1 |
| POSEIDON FOREVER            |          1 |
| POTTER CONNECTICUT          |          1 |
| POTTER CONNECTICUT          |          1 |
| PREJUDICE OLEANDER          |          1 |
| PREJUDICE OLEANDER          |          1 |
| PREJUDICE OLEANDER          |          1 |
| PREJUDICE OLEANDER          |          1 |
| PRESIDENT BANG              |          1 |
| PRESIDENT BANG              |          1 |
| PRIDE ALAMO                 |          1 |
| PRIDE ALAMO                 |          1 |
| PRIMARY GLASS               |          1 |
| PRIMARY GLASS               |          1 |
| PRIMARY GLASS               |          1 |
| PRIMARY GLASS               |          1 |
| PRINCESS GIANT              |          1 |
| PRINCESS GIANT              |          1 |
| PRINCESS GIANT              |          1 |
| PRINCESS GIANT              |          1 |
| PRIVATE DROP                |          1 |
| PRIVATE DROP                |          1 |
| PULP BEVERLY                |          1 |
| PULP BEVERLY                |          1 |
| PULP BEVERLY                |          1 |
| PULP BEVERLY                |          1 |
| PURE RUNNER                 |          1 |
| PURE RUNNER                 |          1 |
| PURPLE MOVIE                |          1 |
| PURPLE MOVIE                |          1 |
| PURPLE MOVIE                |          1 |
| PURPLE MOVIE                |          1 |
| QUEEN LUKE                  |          1 |
| QUEEN LUKE                  |          1 |
| QUEST MUSSOLINI             |          1 |
| QUEST MUSSOLINI             |          1 |
| QUILLS BULL                 |          1 |
| QUILLS BULL                 |          1 |
| RACER EGG                   |          1 |
| RACER EGG                   |          1 |
| RAGE GAMES                  |          1 |
| RAGE GAMES                  |          1 |
| RAGE GAMES                  |          1 |
| RAGE GAMES                  |          1 |
| RANGE MOONWALKER            |          1 |
| RANGE MOONWALKER            |          1 |
| RANGE MOONWALKER            |          1 |
| RANGE MOONWALKER            |          1 |
| REAP UNFAITHFUL             |          1 |
| REAP UNFAITHFUL             |          1 |
| REAR TRADING                |          1 |
| REAR TRADING                |          1 |
| RECORDS ZORRO               |          1 |
| RECORDS ZORRO               |          1 |
| REDEMPTION COMFORTS         |          1 |
| REDEMPTION COMFORTS         |          1 |
| REDEMPTION COMFORTS         |          1 |
| REDS POCUS                  |          1 |
| REDS POCUS                  |          1 |
| REEF SALUTE                 |          1 |
| REEF SALUTE                 |          1 |
| REIGN GENTLEMEN             |          1 |
| REIGN GENTLEMEN             |          1 |
| REIGN GENTLEMEN             |          1 |
| REIGN GENTLEMEN             |          1 |
| REMEMBER DIARY              |          1 |
| REMEMBER DIARY              |          1 |
| REQUIEM TYCOON              |          1 |
| REQUIEM TYCOON              |          1 |
| REQUIEM TYCOON              |          1 |
| RESURRECTION SILVERADO      |          1 |
| RESURRECTION SILVERADO      |          1 |
| REUNION WITCHES             |          1 |
| REUNION WITCHES             |          1 |
| REUNION WITCHES             |          1 |
| RIDGEMONT SUBMARINE         |          1 |
| RIDGEMONT SUBMARINE         |          1 |
| RIDGEMONT SUBMARINE         |          1 |
| RIDGEMONT SUBMARINE         |          1 |
| RINGS HEARTBREAKERS         |          1 |
| RINGS HEARTBREAKERS         |          1 |
| RINGS HEARTBREAKERS         |          1 |
| RINGS HEARTBREAKERS         |          1 |
| RIVER OUTLAW                |          1 |
| RIVER OUTLAW                |          1 |
| RIVER OUTLAW                |          1 |
| RIVER OUTLAW                |          1 |
| ROAD ROXANNE                |          1 |
| ROAD ROXANNE                |          1 |
| ROBBERS JOON                |          1 |
| ROBBERS JOON                |          1 |
| ROBBERS JOON                |          1 |
| ROBBERY BRIGHT              |          1 |
| ROBBERY BRIGHT              |          1 |
| ROBBERY BRIGHT              |          1 |
| ROBBERY BRIGHT              |          1 |
| ROCK INSTINCT               |          1 |
| ROCK INSTINCT               |          1 |
| ROCKETEER MOTHER            |          1 |
| ROCKETEER MOTHER            |          1 |
| ROCKETEER MOTHER            |          1 |
| ROCKETEER MOTHER            |          1 |
| ROCKY WAR                   |          1 |
| ROCKY WAR                   |          1 |
| ROMAN PUNK                  |          1 |
| ROMAN PUNK                  |          1 |
| ROMAN PUNK                  |          1 |
| ROMAN PUNK                  |          1 |
| ROOM ROMAN                  |          1 |
| ROOM ROMAN                  |          1 |
| ROOTS REMEMBER              |          1 |
| ROOTS REMEMBER              |          1 |
| ROSES TREASURE              |          1 |
| ROSES TREASURE              |          1 |
| ROSES TREASURE              |          1 |
| ROSES TREASURE              |          1 |
| ROUGE SQUAD                 |          1 |
| ROUGE SQUAD                 |          1 |
| ROXANNE REBEL               |          1 |
| ROXANNE REBEL               |          1 |
| RUGRATS SHAKESPEARE         |          1 |
| RUGRATS SHAKESPEARE         |          1 |
| RUGRATS SHAKESPEARE         |          1 |
| RUGRATS SHAKESPEARE         |          1 |
| RULES HUMAN                 |          1 |
| RULES HUMAN                 |          1 |
| RUN PACIFIC                 |          1 |
| RUN PACIFIC                 |          1 |
| RUN PACIFIC                 |          1 |
| RUSH GOODFELLAS             |          1 |
| RUSH GOODFELLAS             |          1 |
| RUSH GOODFELLAS             |          1 |
| RUSH GOODFELLAS             |          1 |
| SABRINA MIDNIGHT            |          1 |
| SABRINA MIDNIGHT            |          1 |
| SABRINA MIDNIGHT            |          1 |
| SABRINA MIDNIGHT            |          1 |
| SAGEBRUSH CLUELESS          |          1 |
| SAGEBRUSH CLUELESS          |          1 |
| SAGEBRUSH CLUELESS          |          1 |
| SALUTE APOLLO               |          1 |
| SALUTE APOLLO               |          1 |
| SAMURAI LION                |          1 |
| SAMURAI LION                |          1 |
| SAMURAI LION                |          1 |
| SATISFACTION CONFIDENTIAL   |          1 |
| SATISFACTION CONFIDENTIAL   |          1 |
| SATISFACTION CONFIDENTIAL   |          1 |
| SATURDAY LAMBS              |          1 |
| SATURDAY LAMBS              |          1 |
| SATURDAY LAMBS              |          1 |
| SATURDAY LAMBS              |          1 |
| SATURN NAME                 |          1 |
| SATURN NAME                 |          1 |
| SATURN NAME                 |          1 |
| SATURN NAME                 |          1 |
| SAVANNAH TOWN               |          1 |
| SAVANNAH TOWN               |          1 |
| SAVANNAH TOWN               |          1 |
| SCALAWAG DUCK               |          1 |
| SCALAWAG DUCK               |          1 |
| SCALAWAG DUCK               |          1 |
| SCALAWAG DUCK               |          1 |
| SCARFACE BANG               |          1 |
| SCARFACE BANG               |          1 |
| SCARFACE BANG               |          1 |
| SCORPION APOLLO             |          1 |
| SCORPION APOLLO             |          1 |
| SCORPION APOLLO             |          1 |
| SEA VIRGIN                  |          1 |
| SEA VIRGIN                  |          1 |
| SEA VIRGIN                  |          1 |
| SEA VIRGIN                  |          1 |
| SEABISCUIT PUNK             |          1 |
| SEABISCUIT PUNK             |          1 |
| SEABISCUIT PUNK             |          1 |
| SEABISCUIT PUNK             |          1 |
| SEARCHERS WAIT              |          1 |
| SEARCHERS WAIT              |          1 |
| SEARCHERS WAIT              |          1 |
| SEARCHERS WAIT              |          1 |
| SEATTLE EXPECATIONS         |          1 |
| SEATTLE EXPECATIONS         |          1 |
| SEATTLE EXPECATIONS         |          1 |
| SECRET GROUNDHOG            |          1 |
| SECRET GROUNDHOG            |          1 |
| SECRETARY ROUGE             |          1 |
| SECRETARY ROUGE             |          1 |
| SECRETARY ROUGE             |          1 |
| SECRETS PARADISE            |          1 |
| SECRETS PARADISE            |          1 |
| SECRETS PARADISE            |          1 |
| SECRETS PARADISE            |          1 |
| SHAKESPEARE SADDLE          |          1 |
| SHAKESPEARE SADDLE          |          1 |
| SHAKESPEARE SADDLE          |          1 |
| SHANE DARKNESS              |          1 |
| SHANE DARKNESS              |          1 |
| SHANE DARKNESS              |          1 |
| SHANE DARKNESS              |          1 |
| SHANGHAI TYCOON             |          1 |
| SHANGHAI TYCOON             |          1 |
| SHANGHAI TYCOON             |          1 |
| SHAWSHANK BUBBLE            |          1 |
| SHAWSHANK BUBBLE            |          1 |
| SHAWSHANK BUBBLE            |          1 |
| SHAWSHANK BUBBLE            |          1 |
| SHEPHERD MIDSUMMER          |          1 |
| SHEPHERD MIDSUMMER          |          1 |
| SHEPHERD MIDSUMMER          |          1 |
| SHINING ROSES               |          1 |
| SHINING ROSES               |          1 |
| SHINING ROSES               |          1 |
| SHIP WONDERLAND             |          1 |
| SHIP WONDERLAND             |          1 |
| SHOCK CABIN                 |          1 |
| SHOCK CABIN                 |          1 |
| SHOCK CABIN                 |          1 |
| SHOCK CABIN                 |          1 |
| SHOOTIST SUPERFLY           |          1 |
| SHOOTIST SUPERFLY           |          1 |
| SHOOTIST SUPERFLY           |          1 |
| SHOOTIST SUPERFLY           |          1 |
| SHOW LORD                   |          1 |
| SHOW LORD                   |          1 |
| SHRUNK DIVINE               |          1 |
| SHRUNK DIVINE               |          1 |
| SHRUNK DIVINE               |          1 |
| SHRUNK DIVINE               |          1 |
| SIDE ARK                    |          1 |
| SIDE ARK                    |          1 |
| SIEGE MADRE                 |          1 |
| SIEGE MADRE                 |          1 |
| SIEGE MADRE                 |          1 |
| SIEGE MADRE                 |          1 |
| SIERRA DIVIDE               |          1 |
| SIERRA DIVIDE               |          1 |
| SILENCE KANE                |          1 |
| SILENCE KANE                |          1 |
| SILVERADO GOLDFINGER        |          1 |
| SILVERADO GOLDFINGER        |          1 |
| SIMON NORTH                 |          1 |
| SIMON NORTH                 |          1 |
| SINNERS ATLANTIS            |          1 |
| SINNERS ATLANTIS            |          1 |
| SLACKER LIAISONS            |          1 |
| SLACKER LIAISONS            |          1 |
| SLACKER LIAISONS            |          1 |
| SLACKER LIAISONS            |          1 |
| SLEEPING SUSPECTS           |          1 |
| SLEEPING SUSPECTS           |          1 |
| SLEEPING SUSPECTS           |          1 |
| SLEEPING SUSPECTS           |          1 |
| SLEEPLESS MONSOON           |          1 |
| SLEEPLESS MONSOON           |          1 |
| SLEEPY JAPANESE             |          1 |
| SLEEPY JAPANESE             |          1 |
| SLEEPY JAPANESE             |          1 |
| SLEUTH ORIENT               |          1 |
| SLEUTH ORIENT               |          1 |
| SLEUTH ORIENT               |          1 |
| SLUMS DUCK                  |          1 |
| SLUMS DUCK                  |          1 |
| SLUMS DUCK                  |          1 |
| SLUMS DUCK                  |          1 |
| SMILE EARRING               |          1 |
| SMILE EARRING               |          1 |
| SMILE EARRING               |          1 |
| SMOKING BARBARELLA          |          1 |
| SMOKING BARBARELLA          |          1 |
| SMOKING BARBARELLA          |          1 |
| SNATCH SLIPPER              |          1 |
| SNATCH SLIPPER              |          1 |
| SNATCH SLIPPER              |          1 |
| SNATCHERS MONTEZUMA         |          1 |
| SNATCHERS MONTEZUMA         |          1 |
| SNATCHERS MONTEZUMA         |          1 |
| SNOWMAN ROLLERCOASTER       |          1 |
| SNOWMAN ROLLERCOASTER       |          1 |
| SNOWMAN ROLLERCOASTER       |          1 |
| SNOWMAN ROLLERCOASTER       |          1 |
| SOLDIERS EVOLUTION          |          1 |
| SOLDIERS EVOLUTION          |          1 |
| SOMETHING DUCK              |          1 |
| SOMETHING DUCK              |          1 |
| SOMETHING DUCK              |          1 |
| SONG HEDWIG                 |          1 |
| SONG HEDWIG                 |          1 |
| SONG HEDWIG                 |          1 |
| SONS INTERVIEW              |          1 |
| SONS INTERVIEW              |          1 |
| SONS INTERVIEW              |          1 |
| SONS INTERVIEW              |          1 |
| SOUTH WAIT                  |          1 |
| SOUTH WAIT                  |          1 |
| SOUTH WAIT                  |          1 |
| SPEAKEASY DATE              |          1 |
| SPEAKEASY DATE              |          1 |
| SPEAKEASY DATE              |          1 |
| SPICE SORORITY              |          1 |
| SPICE SORORITY              |          1 |
| SPINAL ROCKY                |          1 |
| SPINAL ROCKY                |          1 |
| SPIRITED CASUALTIES         |          1 |
| SPIRITED CASUALTIES         |          1 |
| SPIRITED CASUALTIES         |          1 |
| SPLASH GUMP                 |          1 |
| SPLASH GUMP                 |          1 |
| SPLASH GUMP                 |          1 |
| SPLASH GUMP                 |          1 |
| SPLENDOR PATTON             |          1 |
| SPLENDOR PATTON             |          1 |
| SPLENDOR PATTON             |          1 |
| SPY MILE                    |          1 |
| SPY MILE                    |          1 |
| SPY MILE                    |          1 |
| SPY MILE                    |          1 |
| SQUAD FISH                  |          1 |
| SQUAD FISH                  |          1 |
| SQUAD FISH                  |          1 |
| STAGECOACH ARMAGEDDON       |          1 |
| STAGECOACH ARMAGEDDON       |          1 |
| STAMPEDE DISTURBING         |          1 |
| STAMPEDE DISTURBING         |          1 |
| STAMPEDE DISTURBING         |          1 |
| STAMPEDE DISTURBING         |          1 |
| STAR OPERATION              |          1 |
| STAR OPERATION              |          1 |
| STAR OPERATION              |          1 |
| STATE WASTELAND             |          1 |
| STATE WASTELAND             |          1 |
| STEEL SANTA                 |          1 |
| STEEL SANTA                 |          1 |
| STEEL SANTA                 |          1 |
| STEEL SANTA                 |          1 |
| STEERS ARMAGEDDON           |          1 |
| STEERS ARMAGEDDON           |          1 |
| STEPMOM DREAM               |          1 |
| STEPMOM DREAM               |          1 |
| STEPMOM DREAM               |          1 |
| STEPMOM DREAM               |          1 |
| STING PERSONAL              |          1 |
| STING PERSONAL              |          1 |
| STING PERSONAL              |          1 |
| STING PERSONAL              |          1 |
| STONE FIRE                  |          1 |
| STONE FIRE                  |          1 |
| STONE FIRE                  |          1 |
| STORM HAPPINESS             |          1 |
| STORM HAPPINESS             |          1 |
| STORM HAPPINESS             |          1 |
| STORM HAPPINESS             |          1 |
| STORY SIDE                  |          1 |
| STORY SIDE                  |          1 |
| STORY SIDE                  |          1 |
| STRAIGHT HOURS              |          1 |
| STRAIGHT HOURS              |          1 |
| STRAIGHT HOURS              |          1 |
| STRANGELOVE DESIRE          |          1 |
| STRANGELOVE DESIRE          |          1 |
| STRANGELOVE DESIRE          |          1 |
| STRANGELOVE DESIRE          |          1 |
| STRANGER STRANGERS          |          1 |
| STRANGER STRANGERS          |          1 |
| STRANGER STRANGERS          |          1 |
| STREAK RIDGEMONT            |          1 |
| STREAK RIDGEMONT            |          1 |
| STREETCAR INTENTIONS        |          1 |
| STREETCAR INTENTIONS        |          1 |
| STREETCAR INTENTIONS        |          1 |
| STREETCAR INTENTIONS        |          1 |
| STRICTLY SCARFACE           |          1 |
| STRICTLY SCARFACE           |          1 |
| STRICTLY SCARFACE           |          1 |
| SUGAR WONKA                 |          1 |
| SUGAR WONKA                 |          1 |
| SUGAR WONKA                 |          1 |
| SUIT WALLS                  |          1 |
| SUIT WALLS                  |          1 |
| SUIT WALLS                  |          1 |
| SUMMER SCARFACE             |          1 |
| SUMMER SCARFACE             |          1 |
| SUMMER SCARFACE             |          1 |
| SUN CONFESSIONS             |          1 |
| SUN CONFESSIONS             |          1 |
| SUN CONFESSIONS             |          1 |
| SUN CONFESSIONS             |          1 |
| SUNDANCE INVASION           |          1 |
| SUNDANCE INVASION           |          1 |
| SUNDANCE INVASION           |          1 |
| SUNDANCE INVASION           |          1 |
| SUNRISE LEAGUE              |          1 |
| SUNRISE LEAGUE              |          1 |
| SUNRISE LEAGUE              |          1 |
| SUNRISE LEAGUE              |          1 |
| SUPER WYOMING               |          1 |
| SUPER WYOMING               |          1 |
| SUPER WYOMING               |          1 |
| SUPER WYOMING               |          1 |
| SUPERFLY TRIP               |          1 |
| SUPERFLY TRIP               |          1 |
| SUPERFLY TRIP               |          1 |
| SUSPECTS QUILLS             |          1 |
| SUSPECTS QUILLS             |          1 |
| SUSPECTS QUILLS             |          1 |
| SUSPECTS QUILLS             |          1 |
| SWARM GOLD                  |          1 |
| SWARM GOLD                  |          1 |
| SWARM GOLD                  |          1 |
| SWARM GOLD                  |          1 |
| SWEDEN SHINING              |          1 |
| SWEDEN SHINING              |          1 |
| SWEETHEARTS SUSPECTS        |          1 |
| SWEETHEARTS SUSPECTS        |          1 |
| SWEETHEARTS SUSPECTS        |          1 |
| SWEETHEARTS SUSPECTS        |          1 |
| TALENTED HOMICIDE           |          1 |
| TALENTED HOMICIDE           |          1 |
| TALENTED HOMICIDE           |          1 |
| TARZAN VIDEOTAPE            |          1 |
| TARZAN VIDEOTAPE            |          1 |
| TAXI KICK                   |          1 |
| TAXI KICK                   |          1 |
| TAXI KICK                   |          1 |
| TELEGRAPH VOYAGE            |          1 |
| TELEGRAPH VOYAGE            |          1 |
| TELEGRAPH VOYAGE            |          1 |
| TELEGRAPH VOYAGE            |          1 |
| TELEMARK HEARTBREAKERS      |          1 |
| TELEMARK HEARTBREAKERS      |          1 |
| TELEMARK HEARTBREAKERS      |          1 |
| TELEMARK HEARTBREAKERS      |          1 |
| TENENBAUMS COMMAND          |          1 |
| TENENBAUMS COMMAND          |          1 |
| TENENBAUMS COMMAND          |          1 |
| TENENBAUMS COMMAND          |          1 |
| TEXAS WATCH                 |          1 |
| TEXAS WATCH                 |          1 |
| THEORY MERMAID              |          1 |
| THEORY MERMAID              |          1 |
| THEORY MERMAID              |          1 |
| THEORY MERMAID              |          1 |
| THIEF PELICAN               |          1 |
| THIEF PELICAN               |          1 |
| THIEF PELICAN               |          1 |
| THIEF PELICAN               |          1 |
| THIN SAGEBRUSH              |          1 |
| THIN SAGEBRUSH              |          1 |
| THIN SAGEBRUSH              |          1 |
| THIN SAGEBRUSH              |          1 |
| TIES HUNGER                 |          1 |
| TIES HUNGER                 |          1 |
| TIES HUNGER                 |          1 |
| TIGHTS DAWN                 |          1 |
| TIGHTS DAWN                 |          1 |
| TIGHTS DAWN                 |          1 |
| TIMBERLAND SKY              |          1 |
| TIMBERLAND SKY              |          1 |
| TIMBERLAND SKY              |          1 |
| TITANIC BOONDOCK            |          1 |
| TITANIC BOONDOCK            |          1 |
| TITANIC BOONDOCK            |          1 |
| TITANS JERK                 |          1 |
| TITANS JERK                 |          1 |
| TITANS JERK                 |          1 |
| TITANS JERK                 |          1 |
| TOMATOES HELLFIGHTERS       |          1 |
| TOMATOES HELLFIGHTERS       |          1 |
| TOMATOES HELLFIGHTERS       |          1 |
| TOMORROW HUSTLER            |          1 |
| TOMORROW HUSTLER            |          1 |
| TOMORROW HUSTLER            |          1 |
| TOMORROW HUSTLER            |          1 |
| TOOTSIE PILOT               |          1 |
| TOOTSIE PILOT               |          1 |
| TORQUE BOUND                |          1 |
| TORQUE BOUND                |          1 |
| TORQUE BOUND                |          1 |
| TORQUE BOUND                |          1 |
| TOURIST PELICAN             |          1 |
| TOURIST PELICAN             |          1 |
| TOURIST PELICAN             |          1 |
| TOWERS HURRICANE            |          1 |
| TOWERS HURRICANE            |          1 |
| TOWERS HURRICANE            |          1 |
| TOWN ARK                    |          1 |
| TOWN ARK                    |          1 |
| TRACY CIDER                 |          1 |
| TRACY CIDER                 |          1 |
| TRACY CIDER                 |          1 |
| TRACY CIDER                 |          1 |
| TRADING PINOCCHIO           |          1 |
| TRADING PINOCCHIO           |          1 |
| TRADING PINOCCHIO           |          1 |
| TRADING PINOCCHIO           |          1 |
| TRAIN BUNCH                 |          1 |
| TRAIN BUNCH                 |          1 |
| TRAINSPOTTING STRANGERS     |          1 |
| TRAINSPOTTING STRANGERS     |          1 |
| TRAINSPOTTING STRANGERS     |          1 |
| TRAMP OTHERS                |          1 |
| TRAMP OTHERS                |          1 |
| TRANSLATION SUMMER          |          1 |
| TRANSLATION SUMMER          |          1 |
| TRANSLATION SUMMER          |          1 |
| TRANSLATION SUMMER          |          1 |
| TRAP GUYS                   |          1 |
| TRAP GUYS                   |          1 |
| TRIP NEWTON                 |          1 |
| TRIP NEWTON                 |          1 |
| TRIP NEWTON                 |          1 |
| TRIP NEWTON                 |          1 |
| TROJAN TOMORROW             |          1 |
| TROJAN TOMORROW             |          1 |
| TROJAN TOMORROW             |          1 |
| TROOPERS METAL              |          1 |
| TROOPERS METAL              |          1 |
| TROOPERS METAL              |          1 |
| TROOPERS METAL              |          1 |
| TROUBLE DATE                |          1 |
| TROUBLE DATE                |          1 |
| TRUMAN CRAZY                |          1 |
| TRUMAN CRAZY                |          1 |
| TRUMAN CRAZY                |          1 |
| TRUMAN CRAZY                |          1 |
| TURN STAR                   |          1 |
| TURN STAR                   |          1 |
| TUXEDO MILE                 |          1 |
| TUXEDO MILE                 |          1 |
| TUXEDO MILE                 |          1 |
| TYCOON GATHERING            |          1 |
| TYCOON GATHERING            |          1 |
| TYCOON GATHERING            |          1 |
| TYCOON GATHERING            |          1 |
| UNBREAKABLE KARATE          |          1 |
| UNBREAKABLE KARATE          |          1 |
| UNBREAKABLE KARATE          |          1 |
| UNCUT SUICIDES              |          1 |
| UNCUT SUICIDES              |          1 |
| UNDEFEATED DALMATIONS       |          1 |
| UNDEFEATED DALMATIONS       |          1 |
| UNDEFEATED DALMATIONS       |          1 |
| UNFORGIVEN ZOOLANDER        |          1 |
| UNFORGIVEN ZOOLANDER        |          1 |
| UNITED PILOT                |          1 |
| UNITED PILOT                |          1 |
| UNITED PILOT                |          1 |
| UPRISING UPTOWN             |          1 |
| UPRISING UPTOWN             |          1 |
| UPRISING UPTOWN             |          1 |
| UPRISING UPTOWN             |          1 |
| UPTOWN YOUNG                |          1 |
| UPTOWN YOUNG                |          1 |
| UPTOWN YOUNG                |          1 |
| USUAL UNTOUCHABLES          |          1 |
| USUAL UNTOUCHABLES          |          1 |
| USUAL UNTOUCHABLES          |          1 |
| USUAL UNTOUCHABLES          |          1 |
| VACATION BOONDOCK           |          1 |
| VACATION BOONDOCK           |          1 |
| VACATION BOONDOCK           |          1 |
| VALLEY PACKER               |          1 |
| VALLEY PACKER               |          1 |
| VAMPIRE WHALE               |          1 |
| VAMPIRE WHALE               |          1 |
| VAMPIRE WHALE               |          1 |
| VANISHING ROCKY             |          1 |
| VANISHING ROCKY             |          1 |
| VARSITY TRIP                |          1 |
| VARSITY TRIP                |          1 |
| VELVET TERMINATOR           |          1 |
| VELVET TERMINATOR           |          1 |
| VELVET TERMINATOR           |          1 |
| VELVET TERMINATOR           |          1 |
| VICTORY ACADEMY             |          1 |
| VICTORY ACADEMY             |          1 |
| VICTORY ACADEMY             |          1 |
| VIDEOTAPE ARSENIC           |          1 |
| VIDEOTAPE ARSENIC           |          1 |
| VIDEOTAPE ARSENIC           |          1 |
| VIDEOTAPE ARSENIC           |          1 |
| VIETNAM SMOOCHY             |          1 |
| VIETNAM SMOOCHY             |          1 |
| VIRGIN DAISY                |          1 |
| VIRGIN DAISY                |          1 |
| VIRGINIAN PLUTO             |          1 |
| VIRGINIAN PLUTO             |          1 |
| VIRGINIAN PLUTO             |          1 |
| VIRGINIAN PLUTO             |          1 |
| VISION TORQUE               |          1 |
| VISION TORQUE               |          1 |
| VOICE PEACH                 |          1 |
| VOICE PEACH                 |          1 |
| VOLCANO TEXAS               |          1 |
| VOLCANO TEXAS               |          1 |
| VOLCANO TEXAS               |          1 |
| VOLCANO TEXAS               |          1 |
| VOYAGE LEGALLY              |          1 |
| VOYAGE LEGALLY              |          1 |
| VOYAGE LEGALLY              |          1 |
| WAGON JAWS                  |          1 |
| WAGON JAWS                  |          1 |
| WAGON JAWS                  |          1 |
| WAIT CIDER                  |          1 |
| WAIT CIDER                  |          1 |
| WAIT CIDER                  |          1 |
| WAIT CIDER                  |          1 |
| WANDA CHAMBER               |          1 |
| WANDA CHAMBER               |          1 |
| WANDA CHAMBER               |          1 |
| WANDA CHAMBER               |          1 |
| WAR NOTTING                 |          1 |
| WAR NOTTING                 |          1 |
| WAR NOTTING                 |          1 |
| WARDROBE PHANTOM            |          1 |
| WARDROBE PHANTOM            |          1 |
| WARDROBE PHANTOM            |          1 |
| WARLOCK WEREWOLF            |          1 |
| WARLOCK WEREWOLF            |          1 |
| WASH HEAVENLY               |          1 |
| WASH HEAVENLY               |          1 |
| WASH HEAVENLY               |          1 |
| WASTELAND DIVINE            |          1 |
| WASTELAND DIVINE            |          1 |
| WASTELAND DIVINE            |          1 |
| WASTELAND DIVINE            |          1 |
| WATCH TRACY                 |          1 |
| WATCH TRACY                 |          1 |
| WATERFRONT DELIVERANCE      |          1 |
| WATERFRONT DELIVERANCE      |          1 |
| WATERFRONT DELIVERANCE      |          1 |
| WATERSHIP FRONTIER          |          1 |
| WATERSHIP FRONTIER          |          1 |
| WEDDING APOLLO              |          1 |
| WEDDING APOLLO              |          1 |
| WEEKEND PERSONAL            |          1 |
| WEEKEND PERSONAL            |          1 |
| WEEKEND PERSONAL            |          1 |
| WEREWOLF LOLA               |          1 |
| WEREWOLF LOLA               |          1 |
| WEREWOLF LOLA               |          1 |
| WEST LION                   |          1 |
| WEST LION                   |          1 |
| WEST LION                   |          1 |
| WEST LION                   |          1 |
| WESTWARD SEABISCUIT         |          1 |
| WESTWARD SEABISCUIT         |          1 |
| WESTWARD SEABISCUIT         |          1 |
| WHALE BIKINI                |          1 |
| WHALE BIKINI                |          1 |
| WHALE BIKINI                |          1 |
| WHALE BIKINI                |          1 |
| WHISPERER GIANT             |          1 |
| WHISPERER GIANT             |          1 |
| WHISPERER GIANT             |          1 |
| WIFE TURN                   |          1 |
| WIFE TURN                   |          1 |
| WIFE TURN                   |          1 |
| WIFE TURN                   |          1 |
| WILD APOLLO                 |          1 |
| WILD APOLLO                 |          1 |
| WILLOW TRACY                |          1 |
| WILLOW TRACY                |          1 |
| WIND PHANTOM                |          1 |
| WIND PHANTOM                |          1 |
| WISDOM WORKER               |          1 |
| WISDOM WORKER               |          1 |
| WISDOM WORKER               |          1 |
| WITCHES PANIC               |          1 |
| WITCHES PANIC               |          1 |
| WITCHES PANIC               |          1 |
| WITCHES PANIC               |          1 |
| WIZARD COLDBLOODED          |          1 |
| WIZARD COLDBLOODED          |          1 |
| WIZARD COLDBLOODED          |          1 |
| WOLVES DESIRE               |          1 |
| WOLVES DESIRE               |          1 |
| WOLVES DESIRE               |          1 |
| WOMEN DORADO                |          1 |
| WOMEN DORADO                |          1 |
| WOMEN DORADO                |          1 |
| WON DARES                   |          1 |
| WON DARES                   |          1 |
| WON DARES                   |          1 |
| WONDERFUL DROP              |          1 |
| WONDERFUL DROP              |          1 |
| WONDERLAND CHRISTMAS        |          1 |
| WONDERLAND CHRISTMAS        |          1 |
| WONDERLAND CHRISTMAS        |          1 |
| WONDERLAND CHRISTMAS        |          1 |
| WONKA SEA                   |          1 |
| WONKA SEA                   |          1 |
| WONKA SEA                   |          1 |
| WONKA SEA                   |          1 |
| WORDS HUNTER                |          1 |
| WORDS HUNTER                |          1 |
| WORKER TARZAN               |          1 |
| WORKER TARZAN               |          1 |
| WORKER TARZAN               |          1 |
| WORKING MICROCOSMOS         |          1 |
| WORKING MICROCOSMOS         |          1 |
| WORKING MICROCOSMOS         |          1 |
| WORKING MICROCOSMOS         |          1 |
| WORST BANGER                |          1 |
| WORST BANGER                |          1 |
| WRONG BEHAVIOR              |          1 |
| WRONG BEHAVIOR              |          1 |
| WRONG BEHAVIOR              |          1 |
| WRONG BEHAVIOR              |          1 |
| WYOMING STORM               |          1 |
| WYOMING STORM               |          1 |
| WYOMING STORM               |          1 |
| YENTL IDAHO                 |          1 |
| YENTL IDAHO                 |          1 |
| YENTL IDAHO                 |          1 |
| YENTL IDAHO                 |          1 |
| YOUNG LANGUAGE              |          1 |
| YOUNG LANGUAGE              |          1 |
| YOUTH KICK                  |          1 |
| YOUTH KICK                  |          1 |
| ZOOLANDER FICTION           |          1 |
| ZOOLANDER FICTION           |          1 |
| ZORRO ARK                   |          1 |
| ZORRO ARK                   |          1 |
| ZORRO ARK                   |          1 |
| ZORRO ARK                   |          1 |
+-----------------------------+------------+
2270 rows in set (0,01 sec)

   ```

7. Listar los nombres y apellidos de los empleados junto con las
direcciones de los almacenes en los que trabajan.

```mysql

select e.nombre, e.apellidos, dir.direccion, dir.direccion2, dir.distrito
from empleado as e
INNER JOIN almacen as a ON e.id_almacen = a.id_almacen
INNER JOIN direccion as dir ON e.id_direccion = dir.id_direccion;
+--------+-----------+----------------------+------------+------------+
| nombre | apellidos | direccion            | direccion2 | distrito   |
+--------+-----------+----------------------+------------+------------+
| Mike   | Hillyer   | 23 Workhaven Lane    | NULL       | Alberta    |
| Jon    | Stephens  | 1411 Lillydale Drive | NULL       | QLD        |
| Pepe   | Spilberg  | 1913 Hanoi Way       |            | Nagasaki   |
| Ada    | Byron     | 1121 Loja Avenue     |            | California |
| Ringo  | Rooksby   | 692 Joliet Street    |            | Attika     |
+--------+-----------+----------------------+------------+------------+
5 rows in set (0,00 sec)

   ```

8. Obtener una lista de pagos realizados, incluyendo el cliente, el
empleado que registró el pago y el alquiler correspondiente.

```mysql

select p.id_pago, c.nombre, e.nombre, a.id_alquiler
from pago as p
inner join alquiler as a ON a.id_alquiler = p.id_alquiler
inner join cliente as c ON c.id_cliente = a.id_cliente
inner join almacen as ac ON ac.id_almacen = c.id_almacen
inner join empleado as e ON e.id_empleado = ac.id_empleado_jefe ;

	

|   16049 | AUSTIN CINTRON        | Jon Stephens |
+---------+-----------------------+--------------+
16049 rows in set (0,03 sec)

   ```

9. Listar las películas y los idiomas en los que están disponibles.

```mysql

select p.titulo, i.nombre
from pelicula as p
INNER JOIN idioma as i on p.id_idioma = i.id_idioma;
-----------------------------------------
| titulo                      | nombre  |
+-----------------------------+---------+
| ACADEMY DINOSAUR            | English |
| ACE GOLDFINGER              | English |
| ADAPTATION HOLES            | English |
| AFFAIR PREJUDICE            | English |
| AFRICAN EGG                 | English |
| AGENT TRUMAN                | English |
| AIRPLANE SIERRA             | English |
| AIRPORT POLLOCK             | English |
| ALABAMA DEVIL               | English |
| ALADDIN CALENDAR            | English |
| ALAMO VIDEOTAPE             | English |
| ALASKA PHANTOM              | English |
| ALI FOREVER                 | English |
| ALICE FANTASIA              | English |
| ALIEN CENTER                | English |
| ALLEY EVOLUTION             | English |
| ALONE TRIP                  | English |
| ALTER VICTORY               | English |
| AMADEUS HOLY                | English |
| AMELIE HELLFIGHTERS         | English |
| AMERICAN CIRCUS             | English |
| AMISTAD MIDSUMMER           | English |
| ANACONDA CONFESSIONS        | English |
| ANALYZE HOOSIERS            | English |
| ANGELS LIFE                 | English |
| ANNIE IDENTITY              | English |
| ANONYMOUS HUMAN             | English |
| ANTHEM LUKE                 | English |
| ANTITRUST TOMATOES          | English |
| ANYTHING SAVANNAH           | English |
| APACHE DIVINE               | English |
| APOCALYPSE FLAMINGOS        | English |
| APOLLO TEEN                 | English |
| ARABIA DOGMA                | English |
| ARACHNOPHOBIA ROLLERCOASTER | English |
| ARGONAUTS TOWN              | English |
| ARIZONA BANG                | English |
| ARK RIDGEMONT               | English |
| ARMAGEDDON LOST             | English |
| ARMY FLINTSTONES            | English |
| ARSENIC INDEPENDENCE        | English |
| ARTIST COLDBLOODED          | English |
| ATLANTIS CAUSE              | English |
| ATTACKS HATE                | English |
| ATTRACTION NEWTON           | English |
| AUTUMN CROW                 | English |
| BABY HALL                   | English |
| BACKLASH UNDEFEATED         | English |
| BADMAN DAWN                 | English |
| BAKED CLEOPATRA             | English |
| BALLOON HOMEWARD            | English |
| BALLROOM MOCKINGBIRD        | English |
| BANG KWAI                   | English |
| BANGER PINOCCHIO            | English |
| BARBARELLA STREETCAR        | English |
| BAREFOOT MANCHURIAN         | English |
| BASIC EASY                  | English |
| BEACH HEARTBREAKERS         | English |
| BEAR GRACELAND              | English |
| BEAST HUNCHBACK             | English |
| BEAUTY GREASE               | English |
| BED HIGHBALL                | English |
| BEDAZZLED MARRIED           | English |
| BEETHOVEN EXORCIST          | English |
| BEHAVIOR RUNAWAY            | English |
| BENEATH RUSH                | English |
| BERETS AGENT                | English |
| BETRAYED REAR               | English |
| BEVERLY OUTLAW              | English |
| BIKINI BORROWERS            | English |
| BILKO ANONYMOUS             | English |
| BILL OTHERS                 | English |
| BINGO TALENTED              | English |
| BIRCH ANTITRUST             | English |
| BIRD INDEPENDENCE           | English |
| BIRDCAGE CASPER             | English |
| BIRDS PERDITION             | English |
| BLACKOUT PRIVATE            | English |
| BLADE POLISH                | English |
| BLANKET BEVERLY             | English |
| BLINDNESS GUN               | English |
| BLOOD ARGONAUTS             | English |
| BLUES INSTINCT              | English |
| BOILED DARES                | English |
| BONNIE HOLOCAUST            | English |
| BOOGIE AMELIE               | English |
| BOONDOCK BALLROOM           | English |
| BORN SPINAL                 | English |
| BORROWERS BEDAZZLED         | English |
| BOULEVARD MOB               | English |
| BOUND CHEAPER               | English |
| BOWFINGER GABLES            | English |
| BRANNIGAN SUNRISE           | English |
| BRAVEHEART HUMAN            | English |
| BREAKFAST GOLDFINGER        | English |
| BREAKING HOME               | English |
| BRIDE INTRIGUE              | English |
| BRIGHT ENCOUNTERS           | English |
| BRINGING HYSTERICAL         | English |
| BROOKLYN DESERT             | English |
| BROTHERHOOD BLANKET         | English |
| BUBBLE GROSSE               | English |
| BUCKET BROTHERHOOD          | English |
| BUGSY SONG                  | English |
| BULL SHAWSHANK              | English |
| BULWORTH COMMANDMENTS       | English |
| BUNCH MINDS                 | English |
| BUTCH PANTHER               | English |
| BUTTERFLY CHOCOLAT          | English |
| CABIN FLASH                 | English |
| CADDYSHACK JEDI             | English |
| CALENDAR GUNFIGHT           | English |
| CALIFORNIA BIRDS            | English |
| CAMELOT VACATION            | English |
| CAMPUS REMEMBER             | English |
| CANDIDATE PERDITION         | English |
| CANDLES GRAPES              | English |
| CANYON STOCK                | English |
| CAPER MOTIONS               | English |
| CARIBBEAN LIBERTY           | English |
| CAROL TEXAS                 | English |
| CARRIE BUNCH                | English |
| CASABLANCA SUPER            | English |
| CASPER DRAGONFLY            | English |
| CASSIDY WYOMING             | English |
| CASUALTIES ENCINO           | English |
| CAT CONEHEADS               | English |
| CATCH AMISTAD               | English |
| CAUSE DATE                  | English |
| CELEBRITY HORN              | English |
| CENTER DINOSAUR             | English |
| CHAINSAW UPTOWN             | English |
| CHAMBER ITALIAN             | English |
| CHAMPION FLATLINERS         | English |
| CHANCE RESURRECTION         | English |
| CHAPLIN LICENSE             | English |
| CHARADE DUFFEL              | English |
| CHARIOTS CONSPIRACY         | English |
| CHASING FIGHT               | English |
| CHEAPER CLYDE               | English |
| CHICAGO NORTH               | English |
| CHICKEN HELLFIGHTERS        | English |
| CHILL LUCK                  | English |
| CHINATOWN GLADIATOR         | English |
| CHISUM BEHAVIOR             | English |
| CHITTY LOCK                 | English |
| CHOCOLAT HARRY              | English |
| CHOCOLATE DUCK              | English |
| CHRISTMAS MOONSHINE         | English |
| CIDER DESIRE                | English |
| CINCINATTI WHISPERER        | English |
| CIRCUS YOUTH                | English |
| CITIZEN SHREK               | English |
| CLASH FREDDY                | English |
| CLEOPATRA DEVIL             | English |
| CLERKS ANGELS               | English |
| CLOCKWORK PARADISE          | English |
| CLONES PINOCCHIO            | English |
| CLOSER BANG                 | English |
| CLUB GRAFFITI               | English |
| CLUE GRAIL                  | English |
| CLUELESS BUCKET             | English |
| CLYDE THEORY                | English |
| COAST RAINBOW               | English |
| COLDBLOODED DARLING         | English |
| COLOR PHILADELPHIA          | English |
| COMA HEAD                   | English |
| COMANCHEROS ENEMY           | English |
| COMFORTS RUSH               | English |
| COMMAND DARLING             | English |
| COMMANDMENTS EXPRESS        | English |
| CONEHEADS SMOOCHY           | English |
| CONFESSIONS MAGUIRE         | English |
| CONFIDENTIAL INTERVIEW      | English |
| CONFUSED CANDLES            | English |
| CONGENIALITY QUEST          | English |
| CONNECTICUT TRAMP           | English |
| CONNECTION MICROCOSMOS      | English |
| CONQUERER NUTS              | English |
| CONSPIRACY SPIRIT           | English |
| CONTACT ANONYMOUS           | English |
| CONTROL ANTHEM              | English |
| CONVERSATION DOWNHILL       | English |
| CORE SUIT                   | English |
| COWBOY DOOM                 | English |
| CRAFT OUTFIELD              | English |
| CRANES RESERVOIR            | English |
| CRAZY HOME                  | English |
| CREATURES SHAKESPEARE       | English |
| CREEPERS KANE               | English |
| CROOKED FROGMEN             | English |
| CROSSING DIVORCE            | English |
| CROSSROADS CASUALTIES       | English |
| CROW GREASE                 | English |
| CROWDS TELEMARK             | English |
| CRUELTY UNFORGIVEN          | English |
| CRUSADE HONEY               | English |
| CRYSTAL BREAKING            | English |
| CUPBOARD SINNERS            | English |
| CURTAIN VIDEOTAPE           | English |
| CYCLONE FAMILY              | English |
| DADDY PITTSBURGH            | English |
| DAISY MENAGERIE             | English |
| DALMATIONS SWEDEN           | English |
| DANCES NONE                 | English |
| DANCING FEVER               | English |
| DANGEROUS UPTOWN            | English |
| DARES PLUTO                 | English |
| DARKNESS WAR                | English |
| DARKO DORADO                | English |
| DARLING BREAKING            | English |
| DARN FORRESTER              | English |
| DATE SPEED                  | English |
| DAUGHTER MADIGAN            | English |
| DAWN POND                   | English |
| DAY UNFAITHFUL              | English |
| DAZED PUNK                  | English |
| DECEIVER BETRAYED           | English |
| DEEP CRUSADE                | English |
| DEER VIRGINIAN              | English |
| DELIVERANCE MULHOLLAND      | English |
| DESERT POSEIDON             | English |
| DESIRE ALIEN                | English |
| DESPERATE TRAINSPOTTING     | English |
| DESTINATION JERK            | English |
| DESTINY SATURDAY            | English |
| DETAILS PACKER              | English |
| DETECTIVE VISION            | English |
| DEVIL DESIRE                | English |
| DIARY PANIC                 | English |
| DINOSAUR SECRETARY          | English |
| DIRTY ACE                   | English |
| DISCIPLE MOTHER             | English |
| DISTURBING SCARFACE         | English |
| DIVIDE MONSTER              | English |
| DIVINE RESURRECTION         | English |
| DIVORCE SHINING             | English |
| DOCTOR GRAIL                | English |
| DOGMA FAMILY                | English |
| DOLLS RAGE                  | English |
| DONNIE ALLEY                | English |
| DOOM DANCING                | English |
| DOORS PRESIDENT             | English |
| DORADO NOTTING              | English |
| DOUBLE WRATH                | English |
| DOUBTFIRE LABYRINTH         | English |
| DOWNHILL ENOUGH             | English |
| DOZEN LION                  | English |
| DRACULA CRYSTAL             | English |
| DRAGON SQUAD                | English |
| DRAGONFLY STRANGERS         | English |
| DREAM PICKUP                | English |
| DRIFTER COMMANDMENTS        | English |
| DRIVER ANNIE                | English |
| DRIVING POLISH              | English |
| DROP WATERFRONT             | English |
| DRUMLINE CYCLONE            | English |
| DRUMS DYNAMITE              | English |
| DUCK RACER                  | English |
| DUDE BLINDNESS              | English |
| DUFFEL APOCALYPSE           | English |
| DUMBO LUST                  | English |
| DURHAM PANKY                | English |
| DWARFS ALTER                | English |
| DYING MAKER                 | English |
| DYNAMITE TARZAN             | English |
| EAGLES PANKY                | English |
| EARLY HOME                  | English |
| EARRING INSTINCT            | English |
| EARTH VISION                | English |
| EASY GLADIATOR              | English |
| EDGE KISSING                | English |
| EFFECT GLADIATOR            | English |
| EGG IGBY                    | English |
| EGYPT TENENBAUMS            | English |
| ELEMENT FREDDY              | English |
| ELEPHANT TROJAN             | English |
| ELF MURDER                  | English |
| ELIZABETH SHANE             | English |
| EMPIRE MALKOVICH            | English |
| ENCINO ELF                  | English |
| ENCOUNTERS CURTAIN          | English |
| ENDING CROWDS               | English |
| ENEMY ODDS                  | English |
| ENGLISH BULWORTH            | English |
| ENOUGH RAGING               | English |
| ENTRAPMENT SATISFACTION     | English |
| ESCAPE METROPOLIS           | English |
| EVE RESURRECTION            | English |
| EVERYONE CRAFT              | English |
| EVOLUTION ALTER             | English |
| EXCITEMENT EVE              | English |
| EXORCIST STING              | English |
| EXPECATIONS NATURAL         | English |
| EXPENDABLE STALLION         | English |
| EXPRESS LONELY              | English |
| EXTRAORDINARY CONQUERER     | English |
| EYES DRIVING                | English |
| FACTORY DRAGON              | English |
| FALCON VOLUME               | English |
| FAMILY SWEET                | English |
| FANTASIA PARK               | English |
| FANTASY TROOPERS            | English |
| FARGO GANDHI                | English |
| FATAL HAUNTED               | English |
| FEATHERS METAL              | English |
| FELLOWSHIP AUTUMN           | English |
| FERRIS MOTHER               | English |
| FEUD FROGMEN                | English |
| FEVER EMPIRE                | English |
| FICTION CHRISTMAS           | English |
| FIDDLER LOST                | English |
| FIDELITY DEVIL              | English |
| FIGHT JAWBREAKER            | English |
| FINDING ANACONDA            | English |
| FIRE WOLVES                 | English |
| FIREBALL PHILADELPHIA       | English |
| FIREHOUSE VIETNAM           | English |
| FISH OPUS                   | English |
| FLAMINGOS CONNECTICUT       | English |
| FLASH WARS                  | English |
| FLATLINERS KILLER           | English |
| FLIGHT LIES                 | English |
| FLINTSTONES HAPPINESS       | English |
| FLOATS GARDEN               | English |
| FLYING HOOK                 | English |
| FOOL MOCKINGBIRD            | English |
| FOREVER CANDIDATE           | English |
| FORREST SONS                | English |
| FORRESTER COMANCHEROS       | English |
| FORWARD TEMPLE              | English |
| FRANKENSTEIN STRANGER       | English |
| FREAKY POCUS                | English |
| FREDDY STORM                | English |
| FREEDOM CLEOPATRA           | English |
| FRENCH HOLIDAY              | English |
| FRIDA SLIPPER               | English |
| FRISCO FORREST              | English |
| FROGMEN BREAKING            | English |
| FRONTIER CABIN              | English |
| FROST HEAD                  | English |
| FUGITIVE MAGUIRE            | English |
| FULL FLATLINERS             | English |
| FURY MURDER                 | English |
| GABLES METROPOLIS           | English |
| GALAXY SWEETHEARTS          | English |
| GAMES BOWFINGER             | English |
| GANDHI KWAI                 | English |
| GANGS PRIDE                 | English |
| GARDEN ISLAND               | English |
| GASLIGHT CRUSADE            | English |
| GATHERING CALENDAR          | English |
| GENTLEMEN STAGE             | English |
| GHOST GROUNDHOG             | English |
| GHOSTBUSTERS ELF            | English |
| GIANT TROOPERS              | English |
| GILBERT PELICAN             | English |
| GILMORE BOILED              | English |
| GLADIATOR WESTWARD          | English |
| GLASS DYING                 | English |
| GLEAMING JAWBREAKER         | English |
| GLORY TRACY                 | English |
| GO PURPLE                   | English |
| GODFATHER DIARY             | English |
| GOLD RIVER                  | English |
| GOLDFINGER SENSIBILITY      | English |
| GOLDMINE TYCOON             | English |
| GONE TROUBLE                | English |
| GOODFELLAS SALUTE           | English |
| GORGEOUS BINGO              | English |
| GOSFORD DONNIE              | English |
| GRACELAND DYNAMITE          | English |
| GRADUATE LORD               | English |
| GRAFFITI LOVE               | English |
| GRAIL FRANKENSTEIN          | English |
| GRAPES FURY                 | English |
| GREASE YOUTH                | English |
| GREATEST NORTH              | English |
| GREEDY ROOTS                | English |
| GREEK EVERYONE              | English |
| GRINCH MASSAGE              | English |
| GRIT CLOCKWORK              | English |
| GROOVE FICTION              | English |
| GROSSE WONDERFUL            | English |
| GROUNDHOG UNCUT             | English |
| GUMP DATE                   | English |
| GUN BONNIE                  | English |
| GUNFIGHT MOON               | English |
| GUNFIGHTER MUSSOLINI        | English |
| GUYS FALCON                 | English |
| HALF OUTFIELD               | English |
| HALL CASSIDY                | English |
| HALLOWEEN NUTS              | English |
| HAMLET WISDOM               | English |
| HANDICAP BOONDOCK           | English |
| HANGING DEEP                | English |
| HANKY OCTOBER               | English |
| HANOVER GALAXY              | English |
| HAPPINESS UNITED            | English |
| HARDLY ROBBERS              | English |
| HAROLD FRENCH               | English |
| HARPER DYING                | English |
| HARRY IDAHO                 | English |
| HATE HANDICAP               | English |
| HAUNTED ANTITRUST           | English |
| HAUNTING PIANIST            | English |
| HAWK CHILL                  | English |
| HEAD STRANGER               | English |
| HEARTBREAKERS BRIGHT        | English |
| HEAVEN FREEDOM              | English |
| HEAVENLY GUN                | English |
| HEAVYWEIGHTS BEAST          | English |
| HEDWIG ALTER                | English |
| HELLFIGHTERS SIERRA         | English |
| HIGH ENCINO                 | English |
| HIGHBALL POTTER             | English |
| HILLS NEIGHBORS             | English |
| HOBBIT ALIEN                | English |
| HOCUS FRIDA                 | English |
| HOLES BRANNIGAN             | English |
| HOLIDAY GAMES               | English |
| HOLLOW JEOPARDY             | English |
| HOLLYWOOD ANONYMOUS         | English |
| HOLOCAUST HIGHBALL          | English |
| HOLY TADPOLE                | English |
| HOME PITY                   | English |
| HOMEWARD CIDER              | English |
| HOMICIDE PEACH              | English |
| HONEY TIES                  | English |
| HOOK CHARIOTS               | English |
| HOOSIERS BIRDCAGE           | English |
| HOPE TOOTSIE                | English |
| HORN WORKING                | English |
| HORROR REIGN                | English |
| HOTEL HAPPINESS             | English |
| HOURS RAGE                  | English |
| HOUSE DYNAMITE              | English |
| HUMAN GRAFFITI              | English |
| HUNCHBACK IMPOSSIBLE        | English |
| HUNGER ROOF                 | English |
| HUNTER ALTER                | English |
| HUNTING MUSKETEERS          | English |
| HURRICANE AFFAIR            | English |
| HUSTLER PARTY               | English |
| HYDE DOCTOR                 | English |
| HYSTERICAL GRAIL            | English |
| ICE CROSSING                | English |
| IDAHO LOVE                  | English |
| IDENTITY LOVER              | English |
| IDOLS SNATCHERS             | English |
| IGBY MAKER                  | English |
| ILLUSION AMELIE             | English |
| IMAGE PRINCESS              | English |
| IMPACT ALADDIN              | English |
| IMPOSSIBLE PREJUDICE        | English |
| INCH JET                    | English |
| INDEPENDENCE HOTEL          | English |
| INDIAN LOVE                 | English |
| INFORMER DOUBLE             | English |
| INNOCENT USUAL              | English |
| INSECTS STONE               | English |
| INSIDER ARIZONA             | English |
| INSTINCT AIRPORT            | English |
| INTENTIONS EMPIRE           | English |
| INTERVIEW LIAISONS          | English |
| INTOLERABLE INTENTIONS      | English |
| INTRIGUE WORST              | English |
| INVASION CYCLONE            | English |
| IRON MOON                   | English |
| ISHTAR ROCKETEER            | English |
| ISLAND EXORCIST             | English |
| ITALIAN AFRICAN             | English |
| JACKET FRISCO               | English |
| JADE BUNCH                  | English |
| JAPANESE RUN                | English |
| JASON TRAP                  | English |
| JAWBREAKER BROOKLYN         | English |
| JAWS HARRY                  | English |
| JEDI BENEATH                | English |
| JEEPERS WEDDING             | English |
| JEKYLL FROGMEN              | English |
| JEOPARDY ENCINO             | English |
| JERICHO MULAN               | English |
| JERK PAYCHECK               | English |
| JERSEY SASSY                | English |
| JET NEIGHBORS               | English |
| JINGLE SAGEBRUSH            | English |
| JOON NORTHWEST              | English |
| JUGGLER HARDLY              | English |
| JUMANJI BLADE               | English |
| JUMPING WRATH               | English |
| JUNGLE CLOSER               | English |
| KANE EXORCIST               | English |
| KARATE MOON                 | English |
| KENTUCKIAN GIANT            | English |
| KICK SAVANNAH               | English |
| KILL BROTHERHOOD            | English |
| KILLER INNOCENT             | English |
| KING EVOLUTION              | English |
| KISS GLORY                  | English |
| KISSING DOLLS               | English |
| KNOCK WARLOCK               | English |
| KRAMER CHOCOLATE            | English |
| KWAI HOMEWARD               | English |
| LABYRINTH LEAGUE            | English |
| LADY STAGE                  | English |
| LADYBUGS ARMAGEDDON         | English |
| LAMBS CINCINATTI            | English |
| LANGUAGE COWBOY             | English |
| LAWLESS VISION              | English |
| LAWRENCE LOVE               | English |
| LEAGUE HELLFIGHTERS         | English |
| LEATHERNECKS DWARFS         | English |
| LEBOWSKI SOLDIERS           | English |
| LEGALLY SECRETARY           | English |
| LEGEND JEDI                 | English |
| LESSON CLEOPATRA            | English |
| LIAISONS SWEET              | English |
| LIBERTY MAGNIFICENT         | English |
| LICENSE WEEKEND             | English |
| LIES TREATMENT              | English |
| LIFE TWISTED                | English |
| LIGHTS DEER                 | English |
| LION UNCUT                  | English |
| LOATHING LEGALLY            | English |
| LOCK REAR                   | English |
| LOLA AGENT                  | English |
| LOLITA WORLD                | English |
| LONELY ELEPHANT             | English |
| LORD ARIZONA                | English |
| LOSE INCH                   | English |
| LOSER HUSTLER               | English |
| LOST BIRD                   | English |
| LOUISIANA HARRY             | English |
| LOVE SUICIDES               | English |
| LOVELY JINGLE               | English |
| LOVER TRUMAN                | English |
| LOVERBOY ATTACKS            | English |
| LUCK OPUS                   | English |
| LUCKY FLYING                | English |
| LUKE MUMMY                  | English |
| LUST LOCK                   | English |
| MADIGAN DORADO              | English |
| MADISON TRAP                | English |
| MADNESS ATTACKS             | English |
| MADRE GABLES                | English |
| MAGIC MALLRATS              | English |
| MAGNIFICENT CHITTY          | English |
| MAGNOLIA FORRESTER          | English |
| MAGUIRE APACHE              | English |
| MAIDEN HOME                 | English |
| MAJESTIC FLOATS             | English |
| MAKER GABLES                | English |
| MALKOVICH PET               | English |
| MALLRATS UNITED             | English |
| MALTESE HOPE                | English |
| MANCHURIAN CURTAIN          | English |
| MANNEQUIN WORST             | English |
| MARRIED GO                  | English |
| MARS ROMAN                  | English |
| MASK PEACH                  | English |
| MASKED BUBBLE               | English |
| MASSACRE USUAL              | English |
| MASSAGE IMAGE               | English |
| MATRIX SNOWMAN              | English |
| MAUDE MOD                   | English |
| MEET CHOCOLATE              | English |
| MEMENTO ZOOLANDER           | English |
| MENAGERIE RUSHMORE          | English |
| MERMAID INSECTS             | English |
| METAL ARMAGEDDON            | English |
| METROPOLIS COMA             | English |
| MICROCOSMOS PARADISE        | English |
| MIDNIGHT WESTWARD           | English |
| MIDSUMMER GROUNDHOG         | English |
| MIGHTY LUCK                 | English |
| MILE MULAN                  | English |
| MILLION ACE                 | English |
| MINDS TRUMAN                | English |
| MINE TITANS                 | English |
| MINORITY KISS               | English |
| MIRACLE VIRTUAL             | English |
| MISSION ZOOLANDER           | English |
| MIXED DOORS                 | English |
| MOB DUFFEL                  | English |
| MOCKINGBIRD HOLLYWOOD       | English |
| MOD SECRETARY               | English |
| MODEL FISH                  | English |
| MODERN DORADO               | English |
| MONEY HAROLD                | English |
| MONSOON CAUSE               | English |
| MONSTER SPARTACUS           | English |
| MONTEREY LABYRINTH          | English |
| MONTEZUMA COMMAND           | English |
| MOON BUNCH                  | English |
| MOONSHINE CABIN             | English |
| MOONWALKER FOOL             | English |
| MOSQUITO ARMAGEDDON         | English |
| MOTHER OLEANDER             | English |
| MOTIONS DETAILS             | English |
| MOULIN WAKE                 | English |
| MOURNING PURPLE             | English |
| MOVIE SHAKESPEARE           | English |
| MULAN MOON                  | English |
| MULHOLLAND BEAST            | English |
| MUMMY CREATURES             | English |
| MUPPET MILE                 | English |
| MURDER ANTITRUST            | English |
| MUSCLE BRIGHT               | English |
| MUSIC BOONDOCK              | English |
| MUSKETEERS WAIT             | English |
| MUSSOLINI SPOILERS          | English |
| MYSTIC TRUMAN               | English |
| NAME DETECTIVE              | English |
| NASH CHOCOLAT               | English |
| NATIONAL STORY              | English |
| NATURAL STOCK               | English |
| NECKLACE OUTBREAK           | English |
| NEIGHBORS CHARADE           | English |
| NEMO CAMPUS                 | English |
| NETWORK PEAK                | English |
| NEWSIES STORY               | English |
| NEWTON LABYRINTH            | English |
| NIGHTMARE CHILL             | English |
| NONE SPIKING                | English |
| NOON PAPI                   | English |
| NORTH TEQUILA               | English |
| NORTHWEST POLISH            | English |
| NOTORIOUS REUNION           | English |
| NOTTING SPEAKEASY           | English |
| NOVOCAINE FLIGHT            | English |
| NUTS TIES                   | English |
| OCTOBER SUBMARINE           | English |
| ODDS BOOGIE                 | English |
| OKLAHOMA JUMANJI            | English |
| OLEANDER CLUE               | English |
| OPEN AFRICAN                | English |
| OPERATION OPERATION         | English |
| OPPOSITE NECKLACE           | English |
| OPUS ICE                    | English |
| ORANGE GRAPES               | English |
| ORDER BETRAYED              | English |
| ORIENT CLOSER               | English |
| OSCAR GOLD                  | English |
| OTHERS SOUP                 | English |
| OUTBREAK DIVINE             | English |
| OUTFIELD MASSACRE           | English |
| OUTLAW HANKY                | English |
| OZ LIAISONS                 | English |
| PACIFIC AMISTAD             | English |
| PACKER MADIGAN              | English |
| PAJAMA JAWBREAKER           | English |
| PANIC CLUB                  | English |
| PANKY SUBMARINE             | English |
| PANTHER REDS                | English |
| PAPI NECKLACE               | English |
| PARADISE SABRINA            | English |
| PARIS WEEKEND               | English |
| PARK CITIZEN                | English |
| PARTY KNOCK                 | English |
| PAST SUICIDES               | English |
| PATHS CONTROL               | English |
| PATIENT SISTER              | English |
| PATRIOT ROMAN               | English |
| PATTON INTERVIEW            | English |
| PAYCHECK WAIT               | English |
| PEACH INNOCENT              | English |
| PEAK FOREVER                | English |
| PEARL DESTINY               | English |
| PELICAN COMFORTS            | English |
| PERDITION FARGO             | English |
| PERFECT GROOVE              | English |
| PERSONAL LADYBUGS           | English |
| PET HAUNTING                | English |
| PHANTOM GLORY               | English |
| PHILADELPHIA WIFE           | English |
| PIANIST OUTFIELD            | English |
| PICKUP DRIVING              | English |
| PILOT HOOSIERS              | English |
| PINOCCHIO SIMON             | English |
| PIRATES ROXANNE             | English |
| PITTSBURGH HUNCHBACK        | English |
| PITY BOUND                  | English |
| PIZZA JUMANJI               | English |
| PLATOON INSTINCT            | English |
| PLUTO OLEANDER              | English |
| POCUS PULP                  | English |
| POLISH BROOKLYN             | English |
| POLLOCK DELIVERANCE         | English |
| POND SEATTLE                | English |
| POSEIDON FOREVER            | English |
| POTLUCK MIXED               | English |
| POTTER CONNECTICUT          | English |
| PREJUDICE OLEANDER          | English |
| PRESIDENT BANG              | English |
| PRIDE ALAMO                 | English |
| PRIMARY GLASS               | English |
| PRINCESS GIANT              | English |
| PRIVATE DROP                | English |
| PRIX UNDEFEATED             | English |
| PSYCHO SHRUNK               | English |
| PULP BEVERLY                | English |
| PUNK DIVORCE                | English |
| PURE RUNNER                 | English |
| PURPLE MOVIE                | English |
| QUEEN LUKE                  | English |
| QUEST MUSSOLINI             | English |
| QUILLS BULL                 | English |
| RACER EGG                   | English |
| RAGE GAMES                  | English |
| RAGING AIRPLANE             | English |
| RAIDERS ANTITRUST           | English |
| RAINBOW SHOCK               | English |
| RANDOM GO                   | English |
| RANGE MOONWALKER            | English |
| REAP UNFAITHFUL             | English |
| REAR TRADING                | English |
| REBEL AIRPORT               | English |
| RECORDS ZORRO               | English |
| REDEMPTION COMFORTS         | English |
| REDS POCUS                  | English |
| REEF SALUTE                 | English |
| REIGN GENTLEMEN             | English |
| REMEMBER DIARY              | English |
| REQUIEM TYCOON              | English |
| RESERVOIR ADAPTATION        | English |
| RESURRECTION SILVERADO      | English |
| REUNION WITCHES             | English |
| RIDER CADDYSHACK            | English |
| RIDGEMONT SUBMARINE         | English |
| RIGHT CRANES                | English |
| RINGS HEARTBREAKERS         | English |
| RIVER OUTLAW                | English |
| ROAD ROXANNE                | English |
| ROBBERS JOON                | English |
| ROBBERY BRIGHT              | English |
| ROCK INSTINCT               | English |
| ROCKETEER MOTHER            | English |
| ROCKY WAR                   | English |
| ROLLERCOASTER BRINGING      | English |
| ROMAN PUNK                  | English |
| ROOF CHAMPION               | English |
| ROOM ROMAN                  | English |
| ROOTS REMEMBER              | English |
| ROSES TREASURE              | English |
| ROUGE SQUAD                 | English |
| ROXANNE REBEL               | English |
| RUGRATS SHAKESPEARE         | English |
| RULES HUMAN                 | English |
| RUN PACIFIC                 | English |
| RUNAWAY TENENBAUMS          | English |
| RUNNER MADIGAN              | English |
| RUSH GOODFELLAS             | English |
| RUSHMORE MERMAID            | English |
| SABRINA MIDNIGHT            | English |
| SADDLE ANTITRUST            | English |
| SAGEBRUSH CLUELESS          | English |
| SAINTS BRIDE                | English |
| SALUTE APOLLO               | English |
| SAMURAI LION                | English |
| SANTA PARIS                 | English |
| SASSY PACKER                | English |
| SATISFACTION CONFIDENTIAL   | English |
| SATURDAY LAMBS              | English |
| SATURN NAME                 | English |
| SAVANNAH TOWN               | English |
| SCALAWAG DUCK               | English |
| SCARFACE BANG               | English |
| SCHOOL JACKET               | English |
| SCISSORHANDS SLUMS          | English |
| SCORPION APOLLO             | English |
| SEA VIRGIN                  | English |
| SEABISCUIT PUNK             | English |
| SEARCHERS WAIT              | English |
| SEATTLE EXPECATIONS         | English |
| SECRET GROUNDHOG            | English |
| SECRETARY ROUGE             | English |
| SECRETS PARADISE            | English |
| SENSE GREEK                 | English |
| SENSIBILITY REAR            | English |
| SEVEN SWARM                 | English |
| SHAKESPEARE SADDLE          | English |
| SHANE DARKNESS              | English |
| SHANGHAI TYCOON             | English |
| SHAWSHANK BUBBLE            | English |
| SHEPHERD MIDSUMMER          | English |
| SHINING ROSES               | English |
| SHIP WONDERLAND             | English |
| SHOCK CABIN                 | English |
| SHOOTIST SUPERFLY           | English |
| SHOW LORD                   | English |
| SHREK LICENSE               | English |
| SHRUNK DIVINE               | English |
| SIDE ARK                    | English |
| SIEGE MADRE                 | English |
| SIERRA DIVIDE               | English |
| SILENCE KANE                | English |
| SILVERADO GOLDFINGER        | English |
| SIMON NORTH                 | English |
| SINNERS ATLANTIS            | English |
| SISTER FREDDY               | English |
| SKY MIRACLE                 | English |
| SLACKER LIAISONS            | English |
| SLEEPING SUSPECTS           | English |
| SLEEPLESS MONSOON           | English |
| SLEEPY JAPANESE             | English |
| SLEUTH ORIENT               | English |
| SLING LUKE                  | English |
| SLIPPER FIDELITY            | English |
| SLUMS DUCK                  | English |
| SMILE EARRING               | English |
| SMOKING BARBARELLA          | English |
| SMOOCHY CONTROL             | English |
| SNATCH SLIPPER              | English |
| SNATCHERS MONTEZUMA         | English |
| SNOWMAN ROLLERCOASTER       | English |
| SOLDIERS EVOLUTION          | English |
| SOMETHING DUCK              | English |
| SONG HEDWIG                 | English |
| SONS INTERVIEW              | English |
| SORORITY QUEEN              | English |
| SOUP WISDOM                 | English |
| SOUTH WAIT                  | English |
| SPARTACUS CHEAPER           | English |
| SPEAKEASY DATE              | English |
| SPEED SUIT                  | English |
| SPICE SORORITY              | English |
| SPIKING ELEMENT             | English |
| SPINAL ROCKY                | English |
| SPIRIT FLINTSTONES          | English |
| SPIRITED CASUALTIES         | English |
| SPLASH GUMP                 | English |
| SPLENDOR PATTON             | English |
| SPOILERS HELLFIGHTERS       | English |
| SPY MILE                    | English |
| SQUAD FISH                  | English |
| STAGE WORLD                 | English |
| STAGECOACH ARMAGEDDON       | English |
| STALLION SUNDANCE           | English |
| STAMPEDE DISTURBING         | English |
| STAR OPERATION              | English |
| STATE WASTELAND             | English |
| STEEL SANTA                 | English |
| STEERS ARMAGEDDON           | English |
| STEPMOM DREAM               | English |
| STING PERSONAL              | English |
| STOCK GLASS                 | English |
| STONE FIRE                  | English |
| STORM HAPPINESS             | English |
| STORY SIDE                  | English |
| STRAIGHT HOURS              | English |
| STRANGELOVE DESIRE          | English |
| STRANGER STRANGERS          | English |
| STRANGERS GRAFFITI          | English |
| STREAK RIDGEMONT            | English |
| STREETCAR INTENTIONS        | English |
| STRICTLY SCARFACE           | English |
| SUBMARINE BED               | English |
| SUGAR WONKA                 | English |
| SUICIDES SILENCE            | English |
| SUIT WALLS                  | English |
| SUMMER SCARFACE             | English |
| SUN CONFESSIONS             | English |
| SUNDANCE INVASION           | English |
| SUNRISE LEAGUE              | English |
| SUNSET RACER                | English |
| SUPER WYOMING               | English |
| SUPERFLY TRIP               | English |
| SUSPECTS QUILLS             | English |
| SWARM GOLD                  | English |
| SWEDEN SHINING              | English |
| SWEET BROTHERHOOD           | English |
| SWEETHEARTS SUSPECTS        | English |
| TADPOLE PARK                | English |
| TALENTED HOMICIDE           | English |
| TARZAN VIDEOTAPE            | English |
| TAXI KICK                   | English |
| TEEN APOLLO                 | English |
| TELEGRAPH VOYAGE            | English |
| TELEMARK HEARTBREAKERS      | English |
| TEMPLE ATTRACTION           | English |
| TENENBAUMS COMMAND          | English |
| TEQUILA PAST                | English |
| TERMINATOR CLUB             | English |
| TEXAS WATCH                 | English |
| THEORY MERMAID              | English |
| THIEF PELICAN               | English |
| THIN SAGEBRUSH              | English |
| TIES HUNGER                 | English |
| TIGHTS DAWN                 | English |
| TIMBERLAND SKY              | English |
| TITANIC BOONDOCK            | English |
| TITANS JERK                 | English |
| TOMATOES HELLFIGHTERS       | English |
| TOMORROW HUSTLER            | English |
| TOOTSIE PILOT               | English |
| TORQUE BOUND                | English |
| TOURIST PELICAN             | English |
| TOWERS HURRICANE            | English |
| TOWN ARK                    | English |
| TRACY CIDER                 | English |
| TRADING PINOCCHIO           | English |
| TRAFFIC HOBBIT              | English |
| TRAIN BUNCH                 | English |
| TRAINSPOTTING STRANGERS     | English |
| TRAMP OTHERS                | English |
| TRANSLATION SUMMER          | English |
| TRAP GUYS                   | English |
| TREASURE COMMAND            | English |
| TREATMENT JEKYLL            | English |
| TRIP NEWTON                 | English |
| TROJAN TOMORROW             | English |
| TROOPERS METAL              | English |
| TROUBLE DATE                | English |
| TRUMAN CRAZY                | English |
| TURN STAR                   | English |
| TUXEDO MILE                 | English |
| TWISTED PIRATES             | English |
| TYCOON GATHERING            | English |
| UNBREAKABLE KARATE          | English |
| UNCUT SUICIDES              | English |
| UNDEFEATED DALMATIONS       | English |
| UNFAITHFUL KILL             | English |
| UNFORGIVEN ZOOLANDER        | English |
| UNITED PILOT                | English |
| UNTOUCHABLES SUNRISE        | English |
| UPRISING UPTOWN             | English |
| UPTOWN YOUNG                | English |
| USUAL UNTOUCHABLES          | English |
| VACATION BOONDOCK           | English |
| VALENTINE VANISHING         | English |
| VALLEY PACKER               | English |
| VAMPIRE WHALE               | English |
| VANILLA DAY                 | English |
| VANISHED GARDEN             | English |
| VANISHING ROCKY             | English |
| VARSITY TRIP                | English |
| VELVET TERMINATOR           | English |
| VERTIGO NORTHWEST           | English |
| VICTORY ACADEMY             | English |
| VIDEOTAPE ARSENIC           | English |
| VIETNAM SMOOCHY             | English |
| VILLAIN DESPERATE           | English |
| VIRGIN DAISY                | English |
| VIRGINIAN PLUTO             | English |
| VIRTUAL SPOILERS            | English |
| VISION TORQUE               | English |
| VOICE PEACH                 | English |
| VOLCANO TEXAS               | English |
| VOLUME HOUSE                | English |
| VOYAGE LEGALLY              | English |
| WAGON JAWS                  | English |
| WAIT CIDER                  | English |
| WAKE JAWS                   | English |
| WALLS ARTIST                | English |
| WANDA CHAMBER               | English |
| WAR NOTTING                 | English |
| WARDROBE PHANTOM            | English |
| WARLOCK WEREWOLF            | English |
| WARS PLUTO                  | English |
| WASH HEAVENLY               | English |
| WASTELAND DIVINE            | English |
| WATCH TRACY                 | English |
| WATERFRONT DELIVERANCE      | English |
| WATERSHIP FRONTIER          | English |
| WEDDING APOLLO              | English |
| WEEKEND PERSONAL            | English |
| WEREWOLF LOLA               | English |
| WEST LION                   | English |
| WESTWARD SEABISCUIT         | English |
| WHALE BIKINI                | English |
| WHISPERER GIANT             | English |
| WIFE TURN                   | English |
| WILD APOLLO                 | English |
| WILLOW TRACY                | English |
| WIND PHANTOM                | English |
| WINDOW SIDE                 | English |
| WISDOM WORKER               | English |
| WITCHES PANIC               | English |
| WIZARD COLDBLOODED          | English |
| WOLVES DESIRE               | English |
| WOMEN DORADO                | English |
| WON DARES                   | English |
| WONDERFUL DROP              | English |
| WONDERLAND CHRISTMAS        | English |
| WONKA SEA                   | English |
| WORDS HUNTER                | English |
| WORKER TARZAN               | English |
| WORKING MICROCOSMOS         | English |
| WORLD LEATHERNECKS          | English |
| WORST BANGER                | English |
| WRATH MILE                  | English |
| WRONG BEHAVIOR              | English |
| WYOMING STORM               | English |
| YENTL IDAHO                 | English |
| YOUNG LANGUAGE              | English |
| YOUTH KICK                  | English |
| ZHIVAGO CORE                | English |
| ZOOLANDER FICTION           | English |
| ZORRO ARK                   | English |
+-----------------------------+---------+
1000 rows in set (0,00 sec)

   ```
10. Encontrar todos los empleados y los almacenes que gestionan.
```mysql
SELECT e.nombre, e.apellidos, a.id_almacen
FROM empleado as e
LEFT JOIN almacen as a ON e.id_empleado = a.id_empleado.jefe;
+--------+-----------+------------+
| nombre | apellidos | id_almacen |
+--------+-----------+------------+
| Mike   | Hillyer   |       NULL |
| Jon    | Stephens  |          2 |
| Pepe   | Spilberg  |       NULL |
| Ada    | Byron     |       NULL |
| Ringo  | Rooksby   |          1 |
+--------+-----------+------------+

5 rows in set (0.00 sec)
   ```

11. Obtener los títulos de las películas que nunca han sido
alquiladas.

```mysql
SELECT 
	p.titulo,
	a.id_alquiler
FROM 
	pelicula AS p
LEFT JOIN
	inventario AS i ON i.id_pelicula  = p.id_pelicula  
LEFT JOIN 
	alquiler AS a ON a.id_inventario = i.id_inventario 
WHERE 
	a.id_inventario IS NULL;
	
+------------------------+-------------+
| titulo                 | id_alquiler |
+------------------------+-------------+
| ACADEMY DINOSAUR       |        NULL |
| ALICE FANTASIA         |        NULL |
| APOLLO TEEN            |        NULL |
| ARGONAUTS TOWN         |        NULL |
| VILLAIN DESPERATE      |        NULL |
| VOLUME HOUSE           |        NULL |
| WAKE JAWS              |        NULL |
| WALLS ARTIST           |        NULL |
+------------------------+-------------+
43 rows in set (0,01 sec)

   ```
12. Listar los empleados que trabajan en el mismo almacén que el
empleado con id_empleado = 1.

```mysql
SELECT e1.nombre, e1.id_almacen
FROM empleado as e
INNER JOIN empleado as e1 ON e.id_almacen = e1.id_almacen
WHERE e.id_empleado = 1;
+--------+------------+
| nombre | id_almacen |
+--------+------------+
| Mike   |          2 |
| Jon    |          2 |
| Pepe   |          2 |
+--------+------------+
3 rows in set (0,00 sec)
   ```

13. Encontrar el nombre de las ciudades que no tienen ningún
cliente registrado.
```
SELECT c.nombre
FROM ciudad as c
left JOIN direccion as d on c.id_ciudad = d.id_ciudad
left JOIN cliente as cli on cli.id_direccion = d.id_direccion
where d.id_ciudad IS NULL AND cli.id_direccion IS NULL;
+----------------------------+
| nombre                     |
+----------------------------+
| A Corua (La Corua)         |
| Abha                       |
| Abu Dhabi                  |
| Acua                       |
| Adana                      |
| Addis Abeba                |
| Aden                       |
| Adoni                      |
| Ahmadnagar                 |
| Akishima                   |
| Akron                      |
| al-Ayn                     |
| al-Hawiya                  |
| al-Manama                  |
| al-Qadarif                 |
| al-Qatif                   |
| Allappuzha (Alleppey)      |
| Allende                    |
| Almirante Brown            |
| Alvorada                   |
| Ambattur                   |
| Amersfoort                 |
| Amroha                     |
| Angra dos Reis             |
| Anpolis                    |
| Antofagasta                |
| Aparecida de Goinia        |
| Apeldoorn                  |
| Araatuba                   |
| Arecibo                    |
| Arlington                  |
| Ashdod                     |
| Ashgabat                   |
| Ashqelon                   |
| Asuncin                    |
| Atinsk                     |
| Atlixco                    |
| Augusta-Richmond County    |
| Aurora                     |
| Avellaneda                 |
| Bag                        |
| Baha Blanca                |
| Baicheng                   |
| Baiyin                     |
| Baku                       |
| Balaiha                    |
| Balikesir                  |
| Balurghat                  |
| Bamenda                    |
| Bandar Seri Begawan        |
| Banjul                     |
| Barcelona                  |
| Basel                      |
| Bat Yam                    |
| Batman                     |
| Batna                      |
| Battambang                 |
| Baybay                     |
| Bayugan                    |
| Bchar                      |
| Beira                      |
| Bellevue                   |
| Belm                       |
| Benguela                   |
| Beni-Mellal                |
| Benin City                 |
| Bergamo                    |
| Berhampore (Baharampur)    |
| Bern                       |
| Bhavnagar                  |
| Bhilwara                   |
| Bhimavaram                 |
| Bhusawal                   |
| Bijapur                    |
| Bilbays                    |
| Binzhou                    |
| Birgunj                    |
| Bislig                     |
| Blumenau                   |
| Boa Vista                  |
| Boksburg                   |
| Botosani                   |
| Botshabelo                 |
| Bradford                   |
| Braslia                    |
| Bratislava                 |
| Brescia                    |
| Brest                      |
| Brindisi                   |
| Brockton                   |
| Bucuresti                  |
| Buenaventura               |
| Bydgoszcz                  |
| Cabuyao                    |
| Callao                     |
| Cam Ranh                   |
| Cape Coral                 |
| Caracas                    |
| Carmen                     |
| Cavite                     |
| Cayenne                    |
| Celaya                     |
| Chandrapur                 |
| Changhwa                   |
| Changzhou                  |
| Chapra                     |
| Charlotte Amalie           |
| Chatsworth                 |
| Cheju                      |
| Chiayi                     |
| Chungho                    |
| Cianjur                    |
| Ciomas                     |
| Ciparay                    |
| Ciudad del Este            |
| Clarksville                |
| Coacalco de Berriozbal     |
| Coatzacoalcos              |
| Compton                    |
| Coquimbo                   |
| Cuauhtmoc                  |
| Cuautla                    |
| Cuernavaca                 |
| Cuman                      |
| Czestochowa                |
| Dadu                       |
| Dallas                     |
| Datong                     |
| Daugavpils                 |
| Daxian                     |
| Dayton                     |
| Deba Habe                  |
| Denizli                    |
| Dhaka                      |
| Dhule (Dhulia)             |
| Dongying                   |
| Donostia-San Sebastin      |
| Dos Quebradas              |
| Duisburg                   |
| Dundee                     |
| Dzerzinsk                  |
| Ede                        |
| Effon-Alaiye               |
| El Alto                    |
| El Fuerte                  |
| El Monte                   |
| Emeishan                   |
| Emmen                      |
| Enshi                      |
| Erlangen                   |
| Escobar                    |
| Eskisehir                  |
| Etawah                     |
| Ezeiza                     |
| Ezhou                      |
| Faaa                       |
| Fengshan                   |
| Firozabad                  |
| Florencia                  |
| Fontana                    |
| Fukuyama                   |
| Funafuti                   |
| Fuyu                       |
| Fuzhou                     |
| Gandhinagar                |
| Garden Grove               |
| Garland                    |
| Gatineau                   |
| Gaziantep                  |
| Gijn                       |
| Gingoog                    |
| Goinia                     |
| Gorontalo                  |
| Grand Prairie              |
| Graz                       |
| Greensboro                 |
| Guadalajara                |
| Guaruj                     |
| guas Lindas de Gois        |
| Gulbarga                   |
| Hagonoy                    |
| Haining                    |
| Haiphong                   |
| Haldia                     |
| Halifax                    |
| Halisahar                  |
| Halle/Saale                |
| Hami                       |
| Hanoi                      |
| Hidalgo                    |
| Higashiosaka               |
| Hino                       |
| Hiroshima                  |
| Hodeida                    |
| Hohhot                     |
| Hoshiarpur                 |
| Hsichuh                    |
| Huaian                     |
| Hubli-Dharwad              |
| Huejutla de Reyes          |
| Huixquilucan               |
| Hunuco                     |
| Ibirit                     |
| Idfu                       |
| Ife                        |
| Ikerre                     |
| Iligan                     |
| Ilorin                     |
| Imus                       |
| Inegl                      |
| Ipoh                       |
| Isesaki                    |
| Ivanovo                    |
| Iwaki                      |
| Iwakuni                    |
| Iwatsuki                   |
| Izumisano                  |
| Jaffna                     |
| Jaipur                     |
| Jakarta                    |
| Jalib al-Shuyukh           |
| Jamalpur                   |
| Jaroslavl                  |
| Jastrzebie-Zdrj            |
| Jedda                      |
| Jelets                     |
| Jinchang                   |
| Jining                     |
| Jinzhou                    |
| Jodhpur                    |
| Johannesburg               |
| Joliet                     |
| Jos Azueta                 |
| Juazeiro do Norte          |
| Juiz de Fora               |
| Junan                      |
| Jurez                      |
| Kabul                      |
| Kakamigahara               |
| Kaliningrad                |
| Kalisz                     |
| Kamakura                   |
| Kamjanets-Podilskyi        |
| Kamyin                     |
| Kanazawa                   |
| Kanchrapara                |
| Kansas City                |
| Karnal                     |
| Katihar                    |
| Kermanshah                 |
| Kilis                      |
| Kimchon                    |
| Kingstown                  |
| Kirovo-Tepetsk             |
| Kisumu                     |
| Kitwe                      |
| Klerksdorp                 |
| Kolpino                    |
| Konotop                    |
| Koriyama                   |
| Korla                      |
| Korolev                    |
| Kowloon and New Kowloon    |
| Ktahya                     |
| Kuching                    |
| Kumbakonam                 |
| Kurgan                     |
| Kursk                      |
| Kuwana                     |
| La Paz                     |
| La Plata                   |
| La Romana                  |
| Laiwu                      |
| Lancaster                  |
| Laohekou                   |
| Lapu-Lapu                  |
| Lausanne                   |
| Le Mans                    |
| Lengshuijiang              |
| Leshan                     |
| Lhokseumawe                |
| Liaocheng                  |
| Lilongwe                   |
| Lima                       |
| Lincoln                    |
| Linz                       |
| Lipetsk                    |
| Livorno                    |
| Ljubertsy                  |
| Loja                       |
| London                     |
| London                     |
| Lublin                     |
| Lubumbashi                 |
| Luzinia                    |
| Madiun                     |
| Mahajanga                  |
| Maikop                     |
| Malm                       |
| Manchester                 |
| Mandaluyong                |
| Mandi Bahauddin            |
| Mannheim                   |
| Maracabo                   |
| Maring                     |
| Matamoros                  |
| Matsue                     |
| Meixian                    |
| Memphis                    |
| Merlo                      |
| Mexicali                   |
| Miraj                      |
| Mit Ghamr                  |
| Miyakonojo                 |
| Mogiljov                   |
| Molodetno                  |
| Monclova                   |
| Monywa                     |
| Moscow                     |
| Mosul                      |
| Mukateve                   |
| Mwanza                     |
| Mwene-Ditu                 |
| Mysore                     |
| Naala-Porto                |
| Nabereznyje Telny          |
| Nador                      |
| Nagaon                     |
| Nagareyama                 |
| Najafabad                  |
| Naju                       |
| Nakhon Sawan               |
| Nam Dinh                   |
| Namibe                     |
| NDjamna                    |
| Newcastle                  |
| Nezahualcyotl              |
| Nha Trang                  |
| Niznekamsk                 |
| Novi Sad                   |
| Novoterkassk               |
| Nukualofa                  |
| Nuuk                       |
| Nyeri                      |
| Ocumare del Tuy            |
| Ogbomosho                  |
| Okara                      |
| Okayama                    |
| Okinawa                    |
| Olomouc                    |
| Omdurman                   |
| Omiya                      |
| Ondo                       |
| Onomichi                   |
| Oshawa                     |
| ostka                      |
| Otsu                       |
| Oulu                       |
| Ourense (Orense)           |
| Owo                        |
| Oyo                        |
| Ozamis                     |
| Paarl                      |
| Pachuca de Soto            |
| Pak Kret                   |
| Palghat (Palakkad)         |
| Pangkal Pinang             |
| Papeete                    |
| Parbhani                   |
| Pathankot                  |
| Patiala                    |
| Patras                     |
| Pavlodar                   |
| Pemalang                   |
| Peoria                     |
| Pereira                    |
| Phnom Penh                 |
| Pingxiang                  |
| Pjatigorsk                 |
| Plock                      |
| Po                         |
| Ponce                      |
| Pontianak                  |
| Poos de Caldas             |
| Portoviejo                 |
| Probolinggo                |
| Pudukkottai                |
| Pune                       |
| Purnea (Purnia)            |
| Purwakarta                 |
| Pyongyang                  |
| Qalyub                     |
| Qinhuangdao                |
| Qomsheh                    |
| Quilmes                    |
| Rae Bareli                 |
| Rajkot                     |
| Rampur                     |
| Rancagua                   |
| Ranchi                     |
| Richmond Hill              |
| Rio Claro                  |
| Rizhao                     |
| Roanoke                    |
| Robamba                    |
| Rockford                   |
| Ruse                       |
| Rustenburg                 |
| s-Hertogenbosch            |
| Saarbrcken                 |
| Saint Louis                |
| Saint-Denis                |
| Salala                     |
| Salamanca                  |
| Salinas                    |
| Salzburg                   |
| Sambhal                    |
| San Felipe de Puerto Plata |
| San Felipe del Progreso    |
| San Juan Bautista Tuxtepec |
| San Lorenzo                |
| San Miguel de Tucumn       |
| Sanaa                      |
| Santa Brbara dOeste        |
| Santa F                    |
| Santa Rosa                 |
| Santiago de los Caballeros |
| Santo Andr                 |
| Sanya                      |
| Satna                      |
| Sawhaj                     |
| Serpuhov                   |
| Shahr-e Kord               |
| Shanwei                    |
| Shaoguan                   |
| Sharja                     |
| Shenzhen                   |
| Shimoga                    |
| Shivapuri                  |
| Shubra al-Khayma           |
| Siegen                     |
| Siliguri (Shiliguri)       |
| Simferopol                 |
| Sincelejo                  |
| Sirjan                     |
| Sivas                      |
| Skikda                     |
| Smolensk                   |
| So Bernardo do Campo       |
| So Leopoldo                |
| Sogamoso                   |
| Sokoto                     |
| Songkhla                   |
| Sorocaba                   |
| Soshanguve                 |
| Sousse                     |
| South Hill                 |
| Southampton                |
| Southport                  |
| Springs                    |
| Stara Zagora               |
| Sterling Heights           |
| Stockport                  |
| Sucre                      |
| Suihua                     |
| Sullana                    |
| Sultanbeyli                |
| Sumqayit                   |
| Sumy                       |
| Sungai Petani              |
| Sunnyvale                  |
| Surakarta                  |
| Syktyvkar                  |
| Syrakusa                   |
| Szkesfehrvr                |
| Tabora                     |
| Tabriz                     |
| Tabuk                      |
| Tafuna                     |
| Taguig                     |
| Taizz                      |
| Talavera                   |
| Tallahassee                |
| Tama                       |
| Tambaram                   |
| Tanauan                    |
| Tandil                     |
| Tanshui                    |
| Tanza                      |
| Tarlac                     |
| Tarsus                     |
| Tartu                      |
| Teboksary                  |
| Tegal                      |
| Tel Aviv-Jaffa             |
| Tete                       |
| Tianjin                    |
| Tiefa                      |
| Tieli                      |
| Tokat                      |
| Tonghae                    |
| Tongliao                   |
| Torren                     |
| Touliu                     |
| Toulon                     |
| Trshavn                    |
| Tsaotun                    |
| Tsuyama                    |
| Tuguegarao                 |
| Tychy                      |
| Udaipur                    |
| Udine                      |
| Ueda                       |
| Uijongbu                   |
| Uluberia                   |
| Urawa                      |
| Uruapan                    |
| Usak                       |
| Usolje-Sibirskoje          |
| Uttarpara-Kotrung          |
| Vaduz                      |
| Valencia                   |
| Valle de la Pascua         |
| Valle de Santiago          |
| Valparai                   |
| Vancouver                  |
| Varanasi (Benares)         |
| Vicente Lpez               |
| Vijayawada                 |
| Vilnius                    |
| Vinh                       |
| Vitria de Santo Anto       |
| Warren                     |
| Weifang                    |
| Witten                     |
| Wroclaw                    |
| Xiangfan                   |
| Xiangtan                   |
| Xintai                     |
| Xinxiang                   |
| Yangor                     |
| Yantai                     |
| Yaound                     |
| Yerevan                    |
| Yinchuan                   |
| Yingkou                    |
| York                       |
| Yuncheng                   |
| Yuzhou                     |
| Zalantun                   |
| Zanzibar                   |
| Zaoyang                    |
| Zapopan                    |
| Zaria                      |
| Zeleznogorsk               |
| Zhezqazghan                |
| Zhoushan                   |
| Ziguinchor                 |
+----------------------------+
558 rows in set (0,00 sec)

   ```
14. Obtener los nombres y apellidos de los actores que han
participado en más de 10 películas.(having)

```mysql
SELECT a.nombre, COUNT(p.id_pelicula) as peliculas
FROM pelicula_actor as p
JOIN actor as a ON a.id_actor = p.id_actor
GROUP BY a.nombre
HAVING peliculas > 10;
+-------------+-----------+
| nombre      | peliculas |
+-------------+-----------+
| PENELOPE    |       102 |
| NICK        |        77 |
| ED          |        83 |
| JENNIFER    |        22 |
| JOHNNY      |        58 |
| BETTE       |        20 |
| GRACE       |        30 |
| MATTHEW     |        89 |
| JOE         |        25 |
| CHRISTIAN   |        79 |
| ZERO        |        25 |
| KARL        |        31 |
| UMA         |        35 |
| VIVIEN      |        65 |
| CUBA        |        77 |
| FRED        |        27 |
| HELEN       |        32 |
| DAN         |        74 |
| BOB         |        25 |
| LUCILLE     |        54 |
| KIRSTEN     |        61 |
| ELVIS       |        26 |
| SANDRA      |        56 |
| CAMERON     |        76 |
| KEVIN       |        54 |
| RIP         |        63 |
| JULIA       |        88 |
| WOODY       |        62 |
| ALEC        |        29 |
| SISSY       |        18 |
| TIM         |        23 |
| MILLA       |        52 |
| AUDREY      |        52 |
| JUDY        |        15 |
| BURT        |        76 |
| VAL         |        35 |
| TOM         |        52 |
| GOLDIE      |        28 |
| JODIE       |        29 |
| KIRK        |        26 |
| REESE       |        65 |
| PARKER      |        24 |
| FRANCES     |        49 |
| ANNE        |        27 |
| NATALIE     |        32 |
| GARY        |        51 |
| CARMEN      |        26 |
| MENA        |        54 |
| FAY         |        73 |
| JUDE        |        30 |
| DUSTIN      |        27 |
| HENRY       |        35 |
| JAYNE       |        90 |
| RAY         |        30 |
| ANGELA      |        69 |
| MARY        |        71 |
| JESSICA     |        23 |
| KENNETH     |       103 |
| MICHELLE    |        23 |
| ADAM        |        40 |
| SEAN        |        59 |
| ANGELINA    |        31 |
| CARY        |        24 |
| GROUCHO     |        86 |
| MAE         |        28 |
| RALPH       |        28 |
| SCARLETT    |        62 |
| BEN         |        56 |
| JAMES       |        31 |
| MINNIE      |        51 |
| GREG        |        27 |
| SPENCER     |        45 |
| CHARLIZE    |        24 |
| CHRISTOPHER |        41 |
| ELLEN       |        25 |
| DARYL       |        61 |
| GENE        |        72 |
| MEG         |        27 |
| CHRIS       |        47 |
| JIM         |        26 |
| SUSAN       |        54 |
| WALTER      |        41 |
| SIDNEY      |        34 |
| GINA        |        42 |
| WARREN      |        66 |
| SYLVESTER   |        22 |
| RUSSELL     |        75 |
| MORGAN      |        79 |
| HARRISON    |        28 |
| RENEE       |        66 |
| LIZA        |        25 |
| SALMA       |        25 |
| JULIANNE    |        32 |
| ALBERT      |        64 |
| CATE        |        58 |
| GRETA       |        59 |
| JANE        |        25 |
| RICHARD     |        30 |
| RITA        |        20 |
| EWAN        |        33 |
| WHOOPI      |        32 |
| JADA        |        31 |
| RIVER       |        31 |
| KIM         |        28 |
| EMILY       |        14 |
| GEOFFREY    |        26 |
| MERYL       |        50 |
| IAN         |        31 |
| LAURA       |        26 |
| HARVEY      |        32 |
| OPRAH       |        25 |
| HUMPHREY    |        55 |
| AL          |        26 |
| LAURENCE    |        26 |
| WILL        |        31 |
| OLYMPIA     |        28 |
| ALAN        |        27 |
| MICHAEL     |        54 |
| WILLIAM     |        27 |
| JON         |        29 |
| LISA        |        23 |
| JEFF        |        25 |
| DEBBIE      |        24 |
| ROCK        |        30 |
| GREGORY     |        30 |
| JOHN        |        29 |
| BELA        |        30 |
| THORA       |        20 |
+-------------+-----------+
128 rows in set (0,01 sec)

15. Encontrar los nombres y apellidos de los clientes que han
realizado un pago mayor a 100.

```mysql
SELECT  c.nombre, c.apellidos
FROM cliente as c
INNER JOIN pago as p ON c.id_cliente = p.id_cliente
WHERE p.total > 100;

Empty set (0,00 sec)
   ```

16. Listar los títulos de las películas lanzadas en el mismo año que
la película con id_pelicula = 2.

```mysql
SELECT p1.titulo
FROM pelicula as p
JOIN pelicula as p1 ON p1.anyo_lanzamiento = p.anyo_lanzamiento
WHERE p.id_pelicula = 2;
+-----------------------------+
| titulo                      |
+-----------------------------+
| ACADEMY DINOSAUR            |
| ACE GOLDFINGER              |
| ADAPTATION HOLES            |
| AFFAIR PREJUDICE            |
| AFRICAN EGG                 |
| AGENT TRUMAN                |
| AIRPLANE SIERRA             |
| AIRPORT POLLOCK             |
| ALABAMA DEVIL               |
| ALADDIN CALENDAR            |
| ALAMO VIDEOTAPE             |
| ALASKA PHANTOM              |
| ALI FOREVER                 |
| ALICE FANTASIA              |
| ALIEN CENTER                |
| ALLEY EVOLUTION             |
| ALONE TRIP                  |
| ALTER VICTORY               |
| AMADEUS HOLY                |
| AMELIE HELLFIGHTERS         |
| AMERICAN CIRCUS             |
| AMISTAD MIDSUMMER           |
| ANACONDA CONFESSIONS        |
| ANALYZE HOOSIERS            |
| ANGELS LIFE                 |
| ANNIE IDENTITY              |
| ANONYMOUS HUMAN             |
| ANTHEM LUKE                 |
| ANTITRUST TOMATOES          |
| ANYTHING SAVANNAH           |
| APACHE DIVINE               |
| APOCALYPSE FLAMINGOS        |
| APOLLO TEEN                 |
| ARABIA DOGMA                |
| ARACHNOPHOBIA ROLLERCOASTER |
| ARGONAUTS TOWN              |
| ARIZONA BANG                |
| ARK RIDGEMONT               |
| ARMAGEDDON LOST             |
| ARMY FLINTSTONES            |
| ARSENIC INDEPENDENCE        |
| ARTIST COLDBLOODED          |
| ATLANTIS CAUSE              |
| ATTACKS HATE                |
| ATTRACTION NEWTON           |
| AUTUMN CROW                 |
| BABY HALL                   |
| BACKLASH UNDEFEATED         |
| BADMAN DAWN                 |
| BAKED CLEOPATRA             |
| BALLOON HOMEWARD            |
| BALLROOM MOCKINGBIRD        |
| BANG KWAI                   |
| BANGER PINOCCHIO            |
| BARBARELLA STREETCAR        |
| BAREFOOT MANCHURIAN         |
| BASIC EASY                  |
| BEACH HEARTBREAKERS         |
| BEAR GRACELAND              |
| BEAST HUNCHBACK             |
| BEAUTY GREASE               |
| BED HIGHBALL                |
| BEDAZZLED MARRIED           |
| BEETHOVEN EXORCIST          |
| BEHAVIOR RUNAWAY            |
| BENEATH RUSH                |
| BERETS AGENT                |
| BETRAYED REAR               |
| BEVERLY OUTLAW              |
| BIKINI BORROWERS            |
| BILKO ANONYMOUS             |
| BILL OTHERS                 |
| BINGO TALENTED              |
| BIRCH ANTITRUST             |
| BIRD INDEPENDENCE           |
| BIRDCAGE CASPER             |
| BIRDS PERDITION             |
| BLACKOUT PRIVATE            |
| BLADE POLISH                |
| BLANKET BEVERLY             |
| BLINDNESS GUN               |
| BLOOD ARGONAUTS             |
| BLUES INSTINCT              |
| BOILED DARES                |
| BONNIE HOLOCAUST            |
| BOOGIE AMELIE               |
| BOONDOCK BALLROOM           |
| BORN SPINAL                 |
| BORROWERS BEDAZZLED         |
| BOULEVARD MOB               |
| BOUND CHEAPER               |
| BOWFINGER GABLES            |
| BRANNIGAN SUNRISE           |
| BRAVEHEART HUMAN            |
| BREAKFAST GOLDFINGER        |
| BREAKING HOME               |
| BRIDE INTRIGUE              |
| BRIGHT ENCOUNTERS           |
| BRINGING HYSTERICAL         |
| BROOKLYN DESERT             |
| BROTHERHOOD BLANKET         |
| BUBBLE GROSSE               |
| BUCKET BROTHERHOOD          |
| BUGSY SONG                  |
| BULL SHAWSHANK              |
| BULWORTH COMMANDMENTS       |
| BUNCH MINDS                 |
| BUTCH PANTHER               |
| BUTTERFLY CHOCOLAT          |
| CABIN FLASH                 |
| CADDYSHACK JEDI             |
| CALENDAR GUNFIGHT           |
| CALIFORNIA BIRDS            |
| CAMELOT VACATION            |
| CAMPUS REMEMBER             |
| CANDIDATE PERDITION         |
| CANDLES GRAPES              |
| CANYON STOCK                |
| CAPER MOTIONS               |
| CARIBBEAN LIBERTY           |
| CAROL TEXAS                 |
| CARRIE BUNCH                |
| CASABLANCA SUPER            |
| CASPER DRAGONFLY            |
| CASSIDY WYOMING             |
| CASUALTIES ENCINO           |
| CAT CONEHEADS               |
| CATCH AMISTAD               |
| CAUSE DATE                  |
| CELEBRITY HORN              |
| CENTER DINOSAUR             |
| CHAINSAW UPTOWN             |
| CHAMBER ITALIAN             |
| CHAMPION FLATLINERS         |
| CHANCE RESURRECTION         |
| CHAPLIN LICENSE             |
| CHARADE DUFFEL              |
| CHARIOTS CONSPIRACY         |
| CHASING FIGHT               |
| CHEAPER CLYDE               |
| CHICAGO NORTH               |
| CHICKEN HELLFIGHTERS        |
| CHILL LUCK                  |
| CHINATOWN GLADIATOR         |
| CHISUM BEHAVIOR             |
| CHITTY LOCK                 |
| CHOCOLAT HARRY              |
| CHOCOLATE DUCK              |
| CHRISTMAS MOONSHINE         |
| CIDER DESIRE                |
| CINCINATTI WHISPERER        |
| CIRCUS YOUTH                |
| CITIZEN SHREK               |
| CLASH FREDDY                |
| CLEOPATRA DEVIL             |
| CLERKS ANGELS               |
| CLOCKWORK PARADISE          |
| CLONES PINOCCHIO            |
| CLOSER BANG                 |
| CLUB GRAFFITI               |
| CLUE GRAIL                  |
| CLUELESS BUCKET             |
| CLYDE THEORY                |
| COAST RAINBOW               |
| COLDBLOODED DARLING         |
| COLOR PHILADELPHIA          |
| COMA HEAD                   |
| COMANCHEROS ENEMY           |
| COMFORTS RUSH               |
| COMMAND DARLING             |
| COMMANDMENTS EXPRESS        |
| CONEHEADS SMOOCHY           |
| CONFESSIONS MAGUIRE         |
| CONFIDENTIAL INTERVIEW      |
| CONFUSED CANDLES            |
| CONGENIALITY QUEST          |
| CONNECTICUT TRAMP           |
| CONNECTION MICROCOSMOS      |
| CONQUERER NUTS              |
| CONSPIRACY SPIRIT           |
| CONTACT ANONYMOUS           |
| CONTROL ANTHEM              |
| CONVERSATION DOWNHILL       |
| CORE SUIT                   |
| COWBOY DOOM                 |
| CRAFT OUTFIELD              |
| CRANES RESERVOIR            |
| CRAZY HOME                  |
| CREATURES SHAKESPEARE       |
| CREEPERS KANE               |
| CROOKED FROGMEN             |
| CROSSING DIVORCE            |
| CROSSROADS CASUALTIES       |
| CROW GREASE                 |
| CROWDS TELEMARK             |
| CRUELTY UNFORGIVEN          |
| CRUSADE HONEY               |
| CRYSTAL BREAKING            |
| CUPBOARD SINNERS            |
| CURTAIN VIDEOTAPE           |
| CYCLONE FAMILY              |
| DADDY PITTSBURGH            |
| DAISY MENAGERIE             |
| DALMATIONS SWEDEN           |
| DANCES NONE                 |
| DANCING FEVER               |
| DANGEROUS UPTOWN            |
| DARES PLUTO                 |
| DARKNESS WAR                |
| DARKO DORADO                |
| DARLING BREAKING            |
| DARN FORRESTER              |
| DATE SPEED                  |
| DAUGHTER MADIGAN            |
| DAWN POND                   |
| DAY UNFAITHFUL              |
| DAZED PUNK                  |
| DECEIVER BETRAYED           |
| DEEP CRUSADE                |
| DEER VIRGINIAN              |
| DELIVERANCE MULHOLLAND      |
| DESERT POSEIDON             |
| DESIRE ALIEN                |
| DESPERATE TRAINSPOTTING     |
| DESTINATION JERK            |
| DESTINY SATURDAY            |
| DETAILS PACKER              |
| DETECTIVE VISION            |
| DEVIL DESIRE                |
| DIARY PANIC                 |
| DINOSAUR SECRETARY          |
| DIRTY ACE                   |
| DISCIPLE MOTHER             |
| DISTURBING SCARFACE         |
| DIVIDE MONSTER              |
| DIVINE RESURRECTION         |
| DIVORCE SHINING             |
| DOCTOR GRAIL                |
| DOGMA FAMILY                |
| DOLLS RAGE                  |
| DONNIE ALLEY                |
| DOOM DANCING                |
| DOORS PRESIDENT             |
| DORADO NOTTING              |
| DOUBLE WRATH                |
| DOUBTFIRE LABYRINTH         |
| DOWNHILL ENOUGH             |
| DOZEN LION                  |
| DRACULA CRYSTAL             |
| DRAGON SQUAD                |
| DRAGONFLY STRANGERS         |
| DREAM PICKUP                |
| DRIFTER COMMANDMENTS        |
| DRIVER ANNIE                |
| DRIVING POLISH              |
| DROP WATERFRONT             |
| DRUMLINE CYCLONE            |
| DRUMS DYNAMITE              |
| DUCK RACER                  |
| DUDE BLINDNESS              |
| DUFFEL APOCALYPSE           |
| DUMBO LUST                  |
| DURHAM PANKY                |
| DWARFS ALTER                |
| DYING MAKER                 |
| DYNAMITE TARZAN             |
| EAGLES PANKY                |
| EARLY HOME                  |
| EARRING INSTINCT            |
| EARTH VISION                |
| EASY GLADIATOR              |
| EDGE KISSING                |
| EFFECT GLADIATOR            |
| EGG IGBY                    |
| EGYPT TENENBAUMS            |
| ELEMENT FREDDY              |
| ELEPHANT TROJAN             |
| ELF MURDER                  |
| ELIZABETH SHANE             |
| EMPIRE MALKOVICH            |
| ENCINO ELF                  |
| ENCOUNTERS CURTAIN          |
| ENDING CROWDS               |
| ENEMY ODDS                  |
| ENGLISH BULWORTH            |
| ENOUGH RAGING               |
| ENTRAPMENT SATISFACTION     |
| ESCAPE METROPOLIS           |
| EVE RESURRECTION            |
| EVERYONE CRAFT              |
| EVOLUTION ALTER             |
| EXCITEMENT EVE              |
| EXORCIST STING              |
| EXPECATIONS NATURAL         |
| EXPENDABLE STALLION         |
| EXPRESS LONELY              |
| EXTRAORDINARY CONQUERER     |
| EYES DRIVING                |
| FACTORY DRAGON              |
| FALCON VOLUME               |
| FAMILY SWEET                |
| FANTASIA PARK               |
| FANTASY TROOPERS            |
| FARGO GANDHI                |
| FATAL HAUNTED               |
| FEATHERS METAL              |
| FELLOWSHIP AUTUMN           |
| FERRIS MOTHER               |
| FEUD FROGMEN                |
| FEVER EMPIRE                |
| FICTION CHRISTMAS           |
| FIDDLER LOST                |
| FIDELITY DEVIL              |
| FIGHT JAWBREAKER            |
| FINDING ANACONDA            |
| FIRE WOLVES                 |
| FIREBALL PHILADELPHIA       |
| FIREHOUSE VIETNAM           |
| FISH OPUS                   |
| FLAMINGOS CONNECTICUT       |
| FLASH WARS                  |
| FLATLINERS KILLER           |
| FLIGHT LIES                 |
| FLINTSTONES HAPPINESS       |
| FLOATS GARDEN               |
| FLYING HOOK                 |
| FOOL MOCKINGBIRD            |
| FOREVER CANDIDATE           |
| FORREST SONS                |
| FORRESTER COMANCHEROS       |
| FORWARD TEMPLE              |
| FRANKENSTEIN STRANGER       |
| FREAKY POCUS                |
| FREDDY STORM                |
| FREEDOM CLEOPATRA           |
| FRENCH HOLIDAY              |
| FRIDA SLIPPER               |
| FRISCO FORREST              |
| FROGMEN BREAKING            |
| FRONTIER CABIN              |
| FROST HEAD                  |
| FUGITIVE MAGUIRE            |
| FULL FLATLINERS             |
| FURY MURDER                 |
| GABLES METROPOLIS           |
| GALAXY SWEETHEARTS          |
| GAMES BOWFINGER             |
| GANDHI KWAI                 |
| GANGS PRIDE                 |
| GARDEN ISLAND               |
| GASLIGHT CRUSADE            |
| GATHERING CALENDAR          |
| GENTLEMEN STAGE             |
| GHOST GROUNDHOG             |
| GHOSTBUSTERS ELF            |
| GIANT TROOPERS              |
| GILBERT PELICAN             |
| GILMORE BOILED              |
| GLADIATOR WESTWARD          |
| GLASS DYING                 |
| GLEAMING JAWBREAKER         |
| GLORY TRACY                 |
| GO PURPLE                   |
| GODFATHER DIARY             |
| GOLD RIVER                  |
| GOLDFINGER SENSIBILITY      |
| GOLDMINE TYCOON             |
| GONE TROUBLE                |
| GOODFELLAS SALUTE           |
| GORGEOUS BINGO              |
| GOSFORD DONNIE              |
| GRACELAND DYNAMITE          |
| GRADUATE LORD               |
| GRAFFITI LOVE               |
| GRAIL FRANKENSTEIN          |
| GRAPES FURY                 |
| GREASE YOUTH                |
| GREATEST NORTH              |
| GREEDY ROOTS                |
| GREEK EVERYONE              |
| GRINCH MASSAGE              |
| GRIT CLOCKWORK              |
| GROOVE FICTION              |
| GROSSE WONDERFUL            |
| GROUNDHOG UNCUT             |
| GUMP DATE                   |
| GUN BONNIE                  |
| GUNFIGHT MOON               |
| GUNFIGHTER MUSSOLINI        |
| GUYS FALCON                 |
| HALF OUTFIELD               |
| HALL CASSIDY                |
| HALLOWEEN NUTS              |
| HAMLET WISDOM               |
| HANDICAP BOONDOCK           |
| HANGING DEEP                |
| HANKY OCTOBER               |
| HANOVER GALAXY              |
| HAPPINESS UNITED            |
| HARDLY ROBBERS              |
| HAROLD FRENCH               |
| HARPER DYING                |
| HARRY IDAHO                 |
| HATE HANDICAP               |
| HAUNTED ANTITRUST           |
| HAUNTING PIANIST            |
| HAWK CHILL                  |
| HEAD STRANGER               |
| HEARTBREAKERS BRIGHT        |
| HEAVEN FREEDOM              |
| HEAVENLY GUN                |
| HEAVYWEIGHTS BEAST          |
| HEDWIG ALTER                |
| HELLFIGHTERS SIERRA         |
| HIGH ENCINO                 |
| HIGHBALL POTTER             |
| HILLS NEIGHBORS             |
| HOBBIT ALIEN                |
| HOCUS FRIDA                 |
| HOLES BRANNIGAN             |
| HOLIDAY GAMES               |
| HOLLOW JEOPARDY             |
| HOLLYWOOD ANONYMOUS         |
| HOLOCAUST HIGHBALL          |
| HOLY TADPOLE                |
| HOME PITY                   |
| HOMEWARD CIDER              |
| HOMICIDE PEACH              |
| HONEY TIES                  |
| HOOK CHARIOTS               |
| HOOSIERS BIRDCAGE           |
| HOPE TOOTSIE                |
| HORN WORKING                |
| HORROR REIGN                |
| HOTEL HAPPINESS             |
| HOURS RAGE                  |
| HOUSE DYNAMITE              |
| HUMAN GRAFFITI              |
| HUNCHBACK IMPOSSIBLE        |
| HUNGER ROOF                 |
| HUNTER ALTER                |
| HUNTING MUSKETEERS          |
| HURRICANE AFFAIR            |
| HUSTLER PARTY               |
| HYDE DOCTOR                 |
| HYSTERICAL GRAIL            |
| ICE CROSSING                |
| IDAHO LOVE                  |
| IDENTITY LOVER              |
| IDOLS SNATCHERS             |
| IGBY MAKER                  |
| ILLUSION AMELIE             |
| IMAGE PRINCESS              |
| IMPACT ALADDIN              |
| IMPOSSIBLE PREJUDICE        |
| INCH JET                    |
| INDEPENDENCE HOTEL          |
| INDIAN LOVE                 |
| INFORMER DOUBLE             |
| INNOCENT USUAL              |
| INSECTS STONE               |
| INSIDER ARIZONA             |
| INSTINCT AIRPORT            |
| INTENTIONS EMPIRE           |
| INTERVIEW LIAISONS          |
| INTOLERABLE INTENTIONS      |
| INTRIGUE WORST              |
| INVASION CYCLONE            |
| IRON MOON                   |
| ISHTAR ROCKETEER            |
| ISLAND EXORCIST             |
| ITALIAN AFRICAN             |
| JACKET FRISCO               |
| JADE BUNCH                  |
| JAPANESE RUN                |
| JASON TRAP                  |
| JAWBREAKER BROOKLYN         |
| JAWS HARRY                  |
| JEDI BENEATH                |
| JEEPERS WEDDING             |
| JEKYLL FROGMEN              |
| JEOPARDY ENCINO             |
| JERICHO MULAN               |
| JERK PAYCHECK               |
| JERSEY SASSY                |
| JET NEIGHBORS               |
| JINGLE SAGEBRUSH            |
| JOON NORTHWEST              |
| JUGGLER HARDLY              |
| JUMANJI BLADE               |
| JUMPING WRATH               |
| JUNGLE CLOSER               |
| KANE EXORCIST               |
| KARATE MOON                 |
| KENTUCKIAN GIANT            |
| KICK SAVANNAH               |
| KILL BROTHERHOOD            |
| KILLER INNOCENT             |
| KING EVOLUTION              |
| KISS GLORY                  |
| KISSING DOLLS               |
| KNOCK WARLOCK               |
| KRAMER CHOCOLATE            |
| KWAI HOMEWARD               |
| LABYRINTH LEAGUE            |
| LADY STAGE                  |
| LADYBUGS ARMAGEDDON         |
| LAMBS CINCINATTI            |
| LANGUAGE COWBOY             |
| LAWLESS VISION              |
| LAWRENCE LOVE               |
| LEAGUE HELLFIGHTERS         |
| LEATHERNECKS DWARFS         |
| LEBOWSKI SOLDIERS           |
| LEGALLY SECRETARY           |
| LEGEND JEDI                 |
| LESSON CLEOPATRA            |
| LIAISONS SWEET              |
| LIBERTY MAGNIFICENT         |
| LICENSE WEEKEND             |
| LIES TREATMENT              |
| LIFE TWISTED                |
| LIGHTS DEER                 |
| LION UNCUT                  |
| LOATHING LEGALLY            |
| LOCK REAR                   |
| LOLA AGENT                  |
| LOLITA WORLD                |
| LONELY ELEPHANT             |
| LORD ARIZONA                |
| LOSE INCH                   |
| LOSER HUSTLER               |
| LOST BIRD                   |
| LOUISIANA HARRY             |
| LOVE SUICIDES               |
| LOVELY JINGLE               |
| LOVER TRUMAN                |
| LOVERBOY ATTACKS            |
| LUCK OPUS                   |
| LUCKY FLYING                |
| LUKE MUMMY                  |
| LUST LOCK                   |
| MADIGAN DORADO              |
| MADISON TRAP                |
| MADNESS ATTACKS             |
| MADRE GABLES                |
| MAGIC MALLRATS              |
| MAGNIFICENT CHITTY          |
| MAGNOLIA FORRESTER          |
| MAGUIRE APACHE              |
| MAIDEN HOME                 |
| MAJESTIC FLOATS             |
| MAKER GABLES                |
| MALKOVICH PET               |
| MALLRATS UNITED             |
| MALTESE HOPE                |
| MANCHURIAN CURTAIN          |
| MANNEQUIN WORST             |
| MARRIED GO                  |
| MARS ROMAN                  |
| MASK PEACH                  |
| MASKED BUBBLE               |
| MASSACRE USUAL              |
| MASSAGE IMAGE               |
| MATRIX SNOWMAN              |
| MAUDE MOD                   |
| MEET CHOCOLATE              |
| MEMENTO ZOOLANDER           |
| MENAGERIE RUSHMORE          |
| MERMAID INSECTS             |
| METAL ARMAGEDDON            |
| METROPOLIS COMA             |
| MICROCOSMOS PARADISE        |
| MIDNIGHT WESTWARD           |
| MIDSUMMER GROUNDHOG         |
| MIGHTY LUCK                 |
| MILE MULAN                  |
| MILLION ACE                 |
| MINDS TRUMAN                |
| MINE TITANS                 |
| MINORITY KISS               |
| MIRACLE VIRTUAL             |
| MISSION ZOOLANDER           |
| MIXED DOORS                 |
| MOB DUFFEL                  |
| MOCKINGBIRD HOLLYWOOD       |
| MOD SECRETARY               |
| MODEL FISH                  |
| MODERN DORADO               |
| MONEY HAROLD                |
| MONSOON CAUSE               |
| MONSTER SPARTACUS           |
| MONTEREY LABYRINTH          |
| MONTEZUMA COMMAND           |
| MOON BUNCH                  |
| MOONSHINE CABIN             |
| MOONWALKER FOOL             |
| MOSQUITO ARMAGEDDON         |
| MOTHER OLEANDER             |
| MOTIONS DETAILS             |
| MOULIN WAKE                 |
| MOURNING PURPLE             |
| MOVIE SHAKESPEARE           |
| MULAN MOON                  |
| MULHOLLAND BEAST            |
| MUMMY CREATURES             |
| MUPPET MILE                 |
| MURDER ANTITRUST            |
| MUSCLE BRIGHT               |
| MUSIC BOONDOCK              |
| MUSKETEERS WAIT             |
| MUSSOLINI SPOILERS          |
| MYSTIC TRUMAN               |
| NAME DETECTIVE              |
| NASH CHOCOLAT               |
| NATIONAL STORY              |
| NATURAL STOCK               |
| NECKLACE OUTBREAK           |
| NEIGHBORS CHARADE           |
| NEMO CAMPUS                 |
| NETWORK PEAK                |
| NEWSIES STORY               |
| NEWTON LABYRINTH            |
| NIGHTMARE CHILL             |
| NONE SPIKING                |
| NOON PAPI                   |
| NORTH TEQUILA               |
| NORTHWEST POLISH            |
| NOTORIOUS REUNION           |
| NOTTING SPEAKEASY           |
| NOVOCAINE FLIGHT            |
| NUTS TIES                   |
| OCTOBER SUBMARINE           |
| ODDS BOOGIE                 |
| OKLAHOMA JUMANJI            |
| OLEANDER CLUE               |
| OPEN AFRICAN                |
| OPERATION OPERATION         |
| OPPOSITE NECKLACE           |
| OPUS ICE                    |
| ORANGE GRAPES               |
| ORDER BETRAYED              |
| ORIENT CLOSER               |
| OSCAR GOLD                  |
| OTHERS SOUP                 |
| OUTBREAK DIVINE             |
| OUTFIELD MASSACRE           |
| OUTLAW HANKY                |
| OZ LIAISONS                 |
| PACIFIC AMISTAD             |
| PACKER MADIGAN              |
| PAJAMA JAWBREAKER           |
| PANIC CLUB                  |
| PANKY SUBMARINE             |
| PANTHER REDS                |
| PAPI NECKLACE               |
| PARADISE SABRINA            |
| PARIS WEEKEND               |
| PARK CITIZEN                |
| PARTY KNOCK                 |
| PAST SUICIDES               |
| PATHS CONTROL               |
| PATIENT SISTER              |
| PATRIOT ROMAN               |
| PATTON INTERVIEW            |
| PAYCHECK WAIT               |
| PEACH INNOCENT              |
| PEAK FOREVER                |
| PEARL DESTINY               |
| PELICAN COMFORTS            |
| PERDITION FARGO             |
| PERFECT GROOVE              |
| PERSONAL LADYBUGS           |
| PET HAUNTING                |
| PHANTOM GLORY               |
| PHILADELPHIA WIFE           |
| PIANIST OUTFIELD            |
| PICKUP DRIVING              |
| PILOT HOOSIERS              |
| PINOCCHIO SIMON             |
| PIRATES ROXANNE             |
| PITTSBURGH HUNCHBACK        |
| PITY BOUND                  |
| PIZZA JUMANJI               |
| PLATOON INSTINCT            |
| PLUTO OLEANDER              |
| POCUS PULP                  |
| POLISH BROOKLYN             |
| POLLOCK DELIVERANCE         |
| POND SEATTLE                |
| POSEIDON FOREVER            |
| POTLUCK MIXED               |
| POTTER CONNECTICUT          |
| PREJUDICE OLEANDER          |
| PRESIDENT BANG              |
| PRIDE ALAMO                 |
| PRIMARY GLASS               |
| PRINCESS GIANT              |
| PRIVATE DROP                |
| PRIX UNDEFEATED             |
| PSYCHO SHRUNK               |
| PULP BEVERLY                |
| PUNK DIVORCE                |
| PURE RUNNER                 |
| PURPLE MOVIE                |
| QUEEN LUKE                  |
| QUEST MUSSOLINI             |
| QUILLS BULL                 |
| RACER EGG                   |
| RAGE GAMES                  |
| RAGING AIRPLANE             |
| RAIDERS ANTITRUST           |
| RAINBOW SHOCK               |
| RANDOM GO                   |
| RANGE MOONWALKER            |
| REAP UNFAITHFUL             |
| REAR TRADING                |
| REBEL AIRPORT               |
| RECORDS ZORRO               |
| REDEMPTION COMFORTS         |
| REDS POCUS                  |
| REEF SALUTE                 |
| REIGN GENTLEMEN             |
| REMEMBER DIARY              |
| REQUIEM TYCOON              |
| RESERVOIR ADAPTATION        |
| RESURRECTION SILVERADO      |
| REUNION WITCHES             |
| RIDER CADDYSHACK            |
| RIDGEMONT SUBMARINE         |
| RIGHT CRANES                |
| RINGS HEARTBREAKERS         |
| RIVER OUTLAW                |
| ROAD ROXANNE                |
| ROBBERS JOON                |
| ROBBERY BRIGHT              |
| ROCK INSTINCT               |
| ROCKETEER MOTHER            |
| ROCKY WAR                   |
| ROLLERCOASTER BRINGING      |
| ROMAN PUNK                  |
| ROOF CHAMPION               |
| ROOM ROMAN                  |
| ROOTS REMEMBER              |
| ROSES TREASURE              |
| ROUGE SQUAD                 |
| ROXANNE REBEL               |
| RUGRATS SHAKESPEARE         |
| RULES HUMAN                 |
| RUN PACIFIC                 |
| RUNAWAY TENENBAUMS          |
| RUNNER MADIGAN              |
| RUSH GOODFELLAS             |
| RUSHMORE MERMAID            |
| SABRINA MIDNIGHT            |
| SADDLE ANTITRUST            |
| SAGEBRUSH CLUELESS          |
| SAINTS BRIDE                |
| SALUTE APOLLO               |
| SAMURAI LION                |
| SANTA PARIS                 |
| SASSY PACKER                |
| SATISFACTION CONFIDENTIAL   |
| SATURDAY LAMBS              |
| SATURN NAME                 |
| SAVANNAH TOWN               |
| SCALAWAG DUCK               |
| SCARFACE BANG               |
| SCHOOL JACKET               |
| SCISSORHANDS SLUMS          |
| SCORPION APOLLO             |
| SEA VIRGIN                  |
| SEABISCUIT PUNK             |
| SEARCHERS WAIT              |
| SEATTLE EXPECATIONS         |
| SECRET GROUNDHOG            |
| SECRETARY ROUGE             |
| SECRETS PARADISE            |
| SENSE GREEK                 |
| SENSIBILITY REAR            |
| SEVEN SWARM                 |
| SHAKESPEARE SADDLE          |
| SHANE DARKNESS              |
| SHANGHAI TYCOON             |
| SHAWSHANK BUBBLE            |
| SHEPHERD MIDSUMMER          |
| SHINING ROSES               |
| SHIP WONDERLAND             |
| SHOCK CABIN                 |
| SHOOTIST SUPERFLY           |
| SHOW LORD                   |
| SHREK LICENSE               |
| SHRUNK DIVINE               |
| SIDE ARK                    |
| SIEGE MADRE                 |
| SIERRA DIVIDE               |
| SILENCE KANE                |
| SILVERADO GOLDFINGER        |
| SIMON NORTH                 |
| SINNERS ATLANTIS            |
| SISTER FREDDY               |
| SKY MIRACLE                 |
| SLACKER LIAISONS            |
| SLEEPING SUSPECTS           |
| SLEEPLESS MONSOON           |
| SLEEPY JAPANESE             |
| SLEUTH ORIENT               |
| SLING LUKE                  |
| SLIPPER FIDELITY            |
| SLUMS DUCK                  |
| SMILE EARRING               |
| SMOKING BARBARELLA          |
| SMOOCHY CONTROL             |
| SNATCH SLIPPER              |
| SNATCHERS MONTEZUMA         |
| SNOWMAN ROLLERCOASTER       |
| SOLDIERS EVOLUTION          |
| SOMETHING DUCK              |
| SONG HEDWIG                 |
| SONS INTERVIEW              |
| SORORITY QUEEN              |
| SOUP WISDOM                 |
| SOUTH WAIT                  |
| SPARTACUS CHEAPER           |
| SPEAKEASY DATE              |
| SPEED SUIT                  |
| SPICE SORORITY              |
| SPIKING ELEMENT             |
| SPINAL ROCKY                |
| SPIRIT FLINTSTONES          |
| SPIRITED CASUALTIES         |
| SPLASH GUMP                 |
| SPLENDOR PATTON             |
| SPOILERS HELLFIGHTERS       |
| SPY MILE                    |
| SQUAD FISH                  |
| STAGE WORLD                 |
| STAGECOACH ARMAGEDDON       |
| STALLION SUNDANCE           |
| STAMPEDE DISTURBING         |
| STAR OPERATION              |
| STATE WASTELAND             |
| STEEL SANTA                 |
| STEERS ARMAGEDDON           |
| STEPMOM DREAM               |
| STING PERSONAL              |
| STOCK GLASS                 |
| STONE FIRE                  |
| STORM HAPPINESS             |
| STORY SIDE                  |
| STRAIGHT HOURS              |
| STRANGELOVE DESIRE          |
| STRANGER STRANGERS          |
| STRANGERS GRAFFITI          |
| STREAK RIDGEMONT            |
| STREETCAR INTENTIONS        |
| STRICTLY SCARFACE           |
| SUBMARINE BED               |
| SUGAR WONKA                 |
| SUICIDES SILENCE            |
| SUIT WALLS                  |
| SUMMER SCARFACE             |
| SUN CONFESSIONS             |
| SUNDANCE INVASION           |
| SUNRISE LEAGUE              |
| SUNSET RACER                |
| SUPER WYOMING               |
| SUPERFLY TRIP               |
| SUSPECTS QUILLS             |
| SWARM GOLD                  |
| SWEDEN SHINING              |
| SWEET BROTHERHOOD           |
| SWEETHEARTS SUSPECTS        |
| TADPOLE PARK                |
| TALENTED HOMICIDE           |
| TARZAN VIDEOTAPE            |
| TAXI KICK                   |
| TEEN APOLLO                 |
| TELEGRAPH VOYAGE            |
| TELEMARK HEARTBREAKERS      |
| TEMPLE ATTRACTION           |
| TENENBAUMS COMMAND          |
| TEQUILA PAST                |
| TERMINATOR CLUB             |
| TEXAS WATCH                 |
| THEORY MERMAID              |
| THIEF PELICAN               |
| THIN SAGEBRUSH              |
| TIES HUNGER                 |
| TIGHTS DAWN                 |
| TIMBERLAND SKY              |
| TITANIC BOONDOCK            |
| TITANS JERK                 |
| TOMATOES HELLFIGHTERS       |
| TOMORROW HUSTLER            |
| TOOTSIE PILOT               |
| TORQUE BOUND                |
| TOURIST PELICAN             |
| TOWERS HURRICANE            |
| TOWN ARK                    |
| TRACY CIDER                 |
| TRADING PINOCCHIO           |
| TRAFFIC HOBBIT              |
| TRAIN BUNCH                 |
| TRAINSPOTTING STRANGERS     |
| TRAMP OTHERS                |
| TRANSLATION SUMMER          |
| TRAP GUYS                   |
| TREASURE COMMAND            |
| TREATMENT JEKYLL            |
| TRIP NEWTON                 |
| TROJAN TOMORROW             |
| TROOPERS METAL              |
| TROUBLE DATE                |
| TRUMAN CRAZY                |
| TURN STAR                   |
| TUXEDO MILE                 |
| TWISTED PIRATES             |
| TYCOON GATHERING            |
| UNBREAKABLE KARATE          |
| UNCUT SUICIDES              |
| UNDEFEATED DALMATIONS       |
| UNFAITHFUL KILL             |
| UNFORGIVEN ZOOLANDER        |
| UNITED PILOT                |
| UNTOUCHABLES SUNRISE        |
| UPRISING UPTOWN             |
| UPTOWN YOUNG                |
| USUAL UNTOUCHABLES          |
| VACATION BOONDOCK           |
| VALENTINE VANISHING         |
| VALLEY PACKER               |
| VAMPIRE WHALE               |
| VANILLA DAY                 |
| VANISHED GARDEN             |
| VANISHING ROCKY             |
| VARSITY TRIP                |
| VELVET TERMINATOR           |
| VERTIGO NORTHWEST           |
| VICTORY ACADEMY             |
| VIDEOTAPE ARSENIC           |
| VIETNAM SMOOCHY             |
| VILLAIN DESPERATE           |
| VIRGIN DAISY                |
| VIRGINIAN PLUTO             |
| VIRTUAL SPOILERS            |
| VISION TORQUE               |
| VOICE PEACH                 |
| VOLCANO TEXAS               |
| VOLUME HOUSE                |
| VOYAGE LEGALLY              |
| WAGON JAWS                  |
| WAIT CIDER                  |
| WAKE JAWS                   |
| WALLS ARTIST                |
| WANDA CHAMBER               |
| WAR NOTTING                 |
| WARDROBE PHANTOM            |
| WARLOCK WEREWOLF            |
| WARS PLUTO                  |
| WASH HEAVENLY               |
| WASTELAND DIVINE            |
| WATCH TRACY                 |
| WATERFRONT DELIVERANCE      |
| WATERSHIP FRONTIER          |
| WEDDING APOLLO              |
| WEEKEND PERSONAL            |
| WEREWOLF LOLA               |
| WEST LION                   |
| WESTWARD SEABISCUIT         |
| WHALE BIKINI                |
| WHISPERER GIANT             |
| WIFE TURN                   |
| WILD APOLLO                 |
| WILLOW TRACY                |
| WIND PHANTOM                |
| WINDOW SIDE                 |
| WISDOM WORKER               |
| WITCHES PANIC               |
| WIZARD COLDBLOODED          |
| WOLVES DESIRE               |
| WOMEN DORADO                |
| WON DARES                   |
| WONDERFUL DROP              |
| WONDERLAND CHRISTMAS        |
| WONKA SEA                   |
| WORDS HUNTER                |
| WORKER TARZAN               |
| WORKING MICROCOSMOS         |
| WORLD LEATHERNECKS          |
| WORST BANGER                |
| WRATH MILE                  |
| WRONG BEHAVIOR              |
| WYOMING STORM               |
| YENTL IDAHO                 |
| YOUNG LANGUAGE              |
| YOUTH KICK                  |
| ZHIVAGO CORE                |
| ZOOLANDER FICTION           |
| ZORRO ARK                   |
+-----------------------------+
1000 rows in set (0,00 sec)


   ```
