# Imparser (Imposter-Parser)

See who the Imposters in an Among Us round are without a modded client (just using Wireshark).

**I do not recommend using this in public rounds**, as this ruins the game for others. This is just a showcase for what is possible if a game is implemented client-side.

## How to use?
Open Wireshark, start listening on your Internet Connection and filter for 
`udp && data.data[0] == 01 && data contains 40:1c:46:00 && frame.len > 100`.

After a round starts a new package should appear. Select the package and right-click on the hex dump which appears at the bottom of the window.

Press "Copy Bytes ...as a Hex Stream" and paste the result in the text field of the [parser](https://imparser.netlify.app/).

Now you should be able to see who the imposters are in the table below.

## Example Hexdump
In case you want to try out the parser without running WireShark + Among Us, you can just copy the hexdump from the example_hexdump.txt file into the parser and try it out that way.

It should look similar to this:

![](example_hexdump.png)
