

setcpm (30/4)

let drum= stack(
s("bd").beat("0,2,4,6,8,10,12,14",16),
s("hh").beat("1,3,5,7,9,11,13,15",16),
s("cp").beat("2,6,10,14",16)
)


//let melody = note("[c4 c4 c4 e4 g4  e4 e4 ~ d4 c4 a3 a3 a3 ~ d4 d4 c4]").sound("metal").legato(1);
//$melody: melody

$drum: drum

let harmony2 = chord("F@4 G@4 Em@4 Am@4").voicing().s("dantranh_tremolo");

$harmony:harmony2
