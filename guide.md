# How to use SoftKVM

SoftKVM connects your Bluetooth devices automatically when you plug in a monitor. This page covers setup, what everything in the window means, and a few tips.

## Quick start

1. **Pair your devices first.** In System Settings → Bluetooth, pair the keyboard, mouse, trackpad, or other devices you want SoftKVM to manage. SoftKVM connects devices that are already paired. It doesn't pair new ones.
2. **Open SoftKVM** and allow Bluetooth access when macOS asks. If it asks to send notifications, allow them so you hear about failed connections.
3. **Pick your monitors.** In the monitor list, select every monitor that should trigger a connection.
4. **Pick your devices.** In the device list, select every device that should connect.
5. **Click Save Configuration.**

That's it. From now on, while the program is running, when a monitor you saved is plugged in SoftKVM will connect your saved devices that aren't already connected.

Only the **saved** configuration drives the automation. Highlighting rows without saving does nothing, and the Save button shows a dot (**• Save Configuration**) while you have unsaved changes.

## Selecting more than one item

Both lists use the standard Mac selection shortcuts. Use them in the monitor list to trigger on several monitors, and in the device list to connect several devices.

| To select... | Do this |
| --- | --- |
| One item | Click it. This replaces any other selection. |
| A run of consecutive items | Click the first item, then hold **Shift** and click the last. Or select one and press **Shift + Up/Down**. |
| Items that aren't next to each other | Hold **Command** and click each one. |
| Deselect a single item | Hold **Command** and click it again. |
| Everything | Click in the list, then press **Command + A**. |

Tips:

- A plain click always starts over with just that one row. To add to your selection, use Shift or Command.
- Clicking the empty space below the rows doesn't clear your selection. Command-click a row to deselect it, or use **Clear Selection**.
- The two lists are independent. Selecting monitors doesn't change which devices are selected.
- With several monitors selected, plugging in **any one** of them triggers the connection.
- With several devices selected, SoftKVM connects them all, and tries each one for about 10 seconds.

## What you see in the window

**The ✓ column.** The narrow first column in each list, with a save icon in its header. A ✓ means that row is part of your saved configuration, so the automation uses it. A highlighted row with no ✓ is selected but not saved yet.

**Device list**

- **Device Name:** the name from System Settings → Bluetooth. If you rename a device there, SoftKVM updates its saved name automatically.
- **MAC Address:** the device's Bluetooth address, which is unique to each device.
- **Active:** 🟢 means the device is connected right now. 🔴 means it isn't. This updates on its own every couple of seconds while the window is open.
- **Dimmed rows:** a device you saved that isn't currently paired with this Mac, for example because you removed it in System Settings. It stays saved and reconnects automatically when it's paired again. Hover over the row for a reminder. To forget it, deselect it and click Save Configuration.

**Monitor list**

- **Monitor Name (Serial: …):** SoftKVM lists every monitor it has seen on this Mac, not just the ones attached right now. You can select a monitor that's currently unplugged.
- **Serial: unknown:** that display doesn't report a serial number. Two identical monitors that both lack one look the same to SoftKVM, so it can't tell them apart.
- **Active:** 🟢 means the monitor is attached right now. 🔴 means it's been seen before but isn't attached.

**Buttons**

- **Refresh device list:** re-reads your Bluetooth devices immediately. The list also refreshes by itself, so you rarely need this.
- **Save Configuration:** saves the current selection as your automation rule.
- **Clear Selection:** removes the highlights in both lists. It does **not** change your saved configuration, and the automation keeps running.

**Menu**

- **Tools → Reset App Data (⇧⌘C):** erases everything SoftKVM has saved, including the saved monitors and devices and its list of known monitors. It asks you to confirm first.

## How the automation works

- It triggers when a saved monitor **newly connects**. Unplugging a monitor, or changing resolution or refresh rate while it stays connected, does nothing.
- It only tries devices that are paired and not already connected.
- If a device can't connect, you get a notification, as long as you've allowed notifications for SoftKVM.

## Tips

- **Keep it running.** Closing the window leaves SoftKVM running in the background, but quitting it (⌘Q) stops the automation. To start it automatically, add it in System Settings → General → Login Items.
- **Turn the automation off without deleting anything else.** Deselect every row in both lists, then click **Save Configuration**. Clear Selection on its own isn't enough.
- **Test it.** Select a monitor and your devices, save, then unplug the monitor and plug it back in. Your saved devices should connect.

## Using one Mac with multiple workstations

Technically you can do this by selecting the superset of monitors and peripherals you would like to connect (and accepting that missing peripherals just won't connect). In the future I may add a profiles feature so you could have e.g. a "Work" and a "Home" profile to make it cleaner and more straightforward. Please email [softkvmapp@gmail.com](mailto:softkvmapp@gmail.com) if that would be useful so I know if it's worth adding!

## Troubleshooting

- **A device isn't in the list.** Pair it in System Settings → Bluetooth first, then click Refresh device list.
- **Nothing happens when I plug in the monitor.** Check that the monitor has a ✓ (select it and click Save Configuration), that at least one device has a ✓, and that SoftKVM is running. Also check System Settings → Privacy & Security → Bluetooth to make sure SoftKVM is allowed.
- **A device won't connect.** Make sure it's turned on, in range, and not connected to another computer. You'll get a notification when a connection fails.

Still stuck? Email [softkvmapp@gmail.com](mailto:softkvmapp@gmail.com).

[Back to home](./)
