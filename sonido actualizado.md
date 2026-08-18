
const { visualid } = createParams('visualid')

setcpm(30/4)

let drum = stack(
 
  s("hh").beat("1,3,5,7,9,11,13,15", 16).visualid("drum_hh"),
  s("cp").beat("2,6,10,14", 16).visualid("drum_cp"),
  s("bd").beat("0,2,4,6,8,10,12,14", 16).visualid("drum_bd")
).bank("RolandTr909")

$drum: stack(drum, drum.osc())

let melody = note(`
  [c5 ~ e5 g5 ~ e5 d5 ~]
  [a4 ~ c5 e5 ~ g5 e5 ~]
  [f5 ~ e5 c5 ~ d5 e5 ~]
  [g5 ~ e5 d5 ~ c5 ~ ~]
`)
  .s("sine")
.s("triangle")
.s("sawtooth")
.s("square")
  .sound("piano")
  .legato(1.5)
  .attack(0.4)
  .release(2)
  .lpf(2000)
  .room(3)
  .visualid("melody")


$melody: stack(melody, melody.osc())

let harmony = note(`
  <[f3,a3,c4,e4]
   [g3,b3,d4,e4]
   [e3,g3,b3,d4]
   [a3,c4,e4,b4]>
`)
  .s("sawtooth")
  .s("square")
  .sound("piano")
  .attack(0.8)
  .release(3)
  .lpf(2000)
  .room(10)
  .visualid("harmony")


$harmony: stack(harmony, harmony.osc())

