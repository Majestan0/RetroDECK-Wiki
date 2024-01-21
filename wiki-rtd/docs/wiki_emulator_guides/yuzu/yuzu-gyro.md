# How to enable Gyro working Gyro in Yuzu

## Steam Deck with Gyro

This is a step by step guide on how to get working Gyro with Yuzu utilizing the Steam Deck's built in gyro.<br>
We are looking into building this feature into RetroDECK in the future.

#### Prerequisites: RetroDECK Steam Deck Controller Layout

Make you have `The Official RetroDECK Steam Deck Controller Layout`  installed and enabled.

If you don't have it read up on `Step 3` from the getting started guide.

[Steam Deck -RetroDECK Installation](../../wiki_devices/steamdeck/steamdeck-start.md).

### Step 1: Install SteamDeckGyroDSU

**NOTE:** If you already have `SteamDeckGyroDSU` installed you can skip this step or just run the `update.sh` from `home/deck/sdgyrodsu` to make sure you have the latest version.

[SteamDeckGyroDSU](https://github.com/kmicki/SteamDeckGyroDSU)

Go to `Desktop Mode` and open the built in terminal `Konsole` from the KDE Menu (Start Menu).

Copy the following command into the terminal and hit enter:

`bash <(curl -sL https://raw.githubusercontent.com/kmicki/SteamDeckGyroDSU/master/pkg/update.sh)`

This will Install SteamDeckGyroDSU and also create a new folder under `HOME` `$HOME/sdgyrodsu/` aka `home/deck/sdgyrodsu`

In that folder you will find two other files that is good to know about:

- `update.sh` - For updating SteamDeckGyroDSU

- `uninstall.sh` - For uninstalling SteamDeckGyroDSU

### Step 2: Go back to gaming mode and launch RetroDECK



## Linux Desktop or Steam Deck Docked with External Gyro Enabled Controllers

**Prerequisites:**

- A gyro enabled external controller.



Check these sources:

https://youtu.be/q-ehLPk9HXI?si=banG3-fO0hxjAofs


https://www.reddit.com/r/SteamDeck/s/kUp6w0fIJA


https://github.com/kmicki/SteamDeckGyroDSU.


   In Desktop mode, install SteamDeckGyroDSU either through EmuDeck (Gyroscope -> More Info in menu) or manually https://github.com/kmicki/SteamDeckGyroDSU. Restart the SteamDeck after installation regardless of which method you used.

   In Gaming mode (will not work in desktop), open a game in Yuzu and open the Menu (F11 with a keyboard or bind a back button to F11)

   From the menu bar select Emulation -> Configure..., then select Controls from the left side bar

   In the top left select Handheld from the Connect Controller dropdown menu (others report that Pro Controller works too)

   From the Input Device dropdown menu just to the right, select Steam Virtual Gamepad 0 (for some reason this defaulted to Keyboard Only for me)

   At the bottom to the left of the controller selector, ensure Motion is checked and click the Configure button underneath

   If not already there, add a server on 127.0.0.1:26760 and click Test to ensure the gyro DSU server is working correctly, then click OK
    Open the Steam overlay, navigate to controller settings, click Edit Layout and set Gyro Behavior to As Directional Pad

   Back on the Yuzu Controls configuration page, you need to click a button that is hidden offscreen. There are two options for how to click it.

  You should still have focus on the Configure button under Motion (highlighted blue), hit tab (on a keyboard or bind tab to a back button) repeatedly to move focus to the next element. Continue to do this until there is focus on the slider bar under the ZR mapping. Click tab one more time to put focus onto the offscreen button that configures the motion mapping. Click enter (on a keyboard or bind enter to a back button).

   Another user found they were able to see the hidden button by setting the game resolution to 1920x1200 for both the internal and external screen, clicking the button, then setting the resolution back after the motion mapping is set. I didn't try this method so I don't know if that was done through the game settings or Yuzu settings, but worth giving it a shot if you know where to change the resolution and/or don't want to have to click tab a bunch.

  Once you've clicked the button (via either method) pick up the Steam Deck and give it a little shake. If everything worked correctly, you should see a wire frame box moving above the image of the Switch/Pro Controller.

  Enjoy your motion controls!
