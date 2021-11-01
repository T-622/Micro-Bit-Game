# Micro-Bit-Game
A simple game made for a TEJ20 tech class with TinkerCad and Micro:Bits:

Designed a simple 2+ player game intended for use with any number of Micro:Bits. Currently running with 4 simultaniously. 

Usage:
- Download .PY files and run Master.py on a single BBC Micro:Bit board. It will act as the master or referee of a game
- Run Player.PY on each board with a modification made to each python file uploaded. Locate [radio.send_value("P1Tot", GlobalCount)] and replace P1 with the number of the player.
- Modify and / or duplicate the Master.py file's line:

  [key = arg0
  Player4Total = arg1
  if key + "" == "P2Tot" + "":
    basic.show_leds("""
      # # # # #
      # # # # #
      # # # # #
      # # # # #
      # # # # #
      """)
    basic.clear_screen()
    basic.show_string("P4:")
    basic.show_number(Player4Total)]

And add or remove the number of blocks matching it based on the number of players; change [basic.show_string("P4:")] to the player number and [Player4Total = arg1] to [Player<#>Total = arg1]
