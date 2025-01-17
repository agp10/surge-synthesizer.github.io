---
layout: page
title: Accessibility Notes
permalink: /accessibility/
noheader: true
toc_levels: 1..4
---

<style>
article h4 {
    font-weight: bold;
}
</style>


{:.no_toc}
# Introduction

As of Surge XT 1.0, both the plugin - as well as standalone version - include accessibility for screen readers
and other assistive technologies on Windows and Mac OS. On this page you’ll find information on how to configure Surge
to work best with a screen reader, as well as some tips on how to navigate around the interface faster.

<br/>
## Table of Contents
{:.no_toc}

* unordered list
{:toc}

<br/>
<br/>
<br/>
<br/>


# Recommended configuration options

The Workflow sub-menu in Surge XT includes a few of options that should be turned on for the best accessibility experience.
To adjust these, after you have opened Surge XT in your DAW (or the standalone), find and press the "Main Menu" button and open the "Workflow" sub-menu.
Once you're there, check the following options, if they're not already turned on:

- **Use keyboard shortcuts** - enables additional keyboard shortcuts to navigate and save patches, adjust parameters and more.
- **Shift + F10 and Edit Parameter Value shortcuts > Follow keyboard focus** - this allows you to bring up context menus on the focused control with Shift+F10.
- **Send additional accessibility announcements** - makes Surge XT speak additional messages when you change patches or wavetables,
add or remove a patch from favorites and use the Undo/Redo features.
- **Add Sub-menus for Modulation Menu Items** - This makes accessing options to Mute, Edit and Clear modulations easier.
- **Announce Patch Browser entries** - this makes the patch search results list accessible on Windows by speaking the selected patch with SAPI,
in order to work around a bug on Windows. This option is not present on Mac OS where the patch list is spoken correctly by VoiceOver.


Depending on the DAW, some of Surge XT's keyboard shortcuts may not get through to the plugin.
If this happens, refer to your DAW's documentation for a way to pass all keyboard input through to the plugin.
For example, in case of REAPER, you will find this option in the "preset menu" button found in the FX dialog. Alternatively, you can change any of Surge XT's keyboard shortcuts by selecting "Edit keyboard shortcuts..." From the Workflow menu (or pressing Alt+B if you have already enabled keyboard shortcuts).

# Useful shortcuts

## Basic navigation

You can navigate Surge XT's interface using the keys you normally would in any other program.
On Windows with Tab/Shift+Tab and the arrow keys, on Mac with VoiceOver commands.
Every control also offers a right-click menu with additional options, which can be accessed with Shift+F10 or VO+Shift+M on Mac.

In addition, you can use Alt+Period/Comma (Windows) or Option+Period/Comma (Mac) to quickly jump the focus between major interface sections. 

Other useful navigation commands worth remembering include:

- Alt/Option+S - change the focused scene
- Alt/Option+1, 2 or 3 - change the selected oscillator
- Alt/Option+M - opens the Modulation List, which allows you to easily add, modify, mute or delete all modulations in the patch from one place.

## Manipulating sliders

When a slider has focus, the following keys can be used:

- Up/Down adjusts the value. Holding Shift makes smaller adjustments, while holding Control (Command on macOS) goes in quantized steps
(for example, semitones when focused on the Pitch slider)
- Home (Fn+Left on Mac keyboards) jumps to slider's maximum value, End (Fn+Right) jumps to the minimum instead.
- Delete (Fn+Backspace on Mac keyboards) resets the slider to its default value.
- Enter opens a dialog allowing you to type in an exact value for a parameter.

## Navigating patches

In addition to pressing the Patch Browser to get a menu of all patches or using the previous/next controls,
a number of keyboard shortcuts are available to make navigating patches easier.

- Previous category: Shift+Left arrow
- Next category: Shift+Right arrow
- Previous patch: Control/Command+Left
- Next patch: Control/Command+Right
- Find patch via textual search: Control/Command+F
- Add/remove patch from favorites: Alt/Option+F. Favorites are available in their own section of the Patch Browser menu


# Platform-specific hints

## macOS and VoiceOver

If you find that the cursor gets stuck in a submenu, either disable cursor tracking by hitting VO+Shift+F3 while you're in the menu,
or set the mouse cursor to ignore VoiceOver in the navigation section of VoiceOver utility.

Sliders can be adjusted using the conventional VoiceOver approach of interacting, but you will find that using Surge XT’s native keystrokes
to move the sliders provide more granular control. See [Manipulating sliders](#manipulating-sliders) section above for more details.

In addition to its standard navigation and interaction keystrokes, VoiceOver's deeper features can boost productivity when navigating
complex applications like Surge XT. A few that you will likely find helpful are VoiceOver Find (VO+F), Item Chooser (VO+I) and Hotspots.
Consult [VoiceOver documentation](https://support.apple.com/guide/voiceover/toc) for more information.



## Windows

### Known issues

There are currently two things to be aware of when using Surge XT on Windows.

- Search results in the Ctrl+F patch typeahead are not visible to screen readers when you arrow through them.
However, Surge XT should speak them with your default Windows voice if the "Announce Patch Browser entries" option is checked in the Workflow menu.
The results will be made accessible to screen readers in a future update.
- When you close a menu, screen readers will not notice the focus change until you tab to a different control.
This appears to be a JUCE bug. For more technical details and updates on this issue, see [issue #6426](https://github.com/surge-synthesizer/surge/issues/6426) in the Surge XT bug tracker.


### Screen reader specific navigation hints

Generally speaking, Surge can be navigated using Tab and Shift+Tab to move focus through controls, arrow keys to adjust the control that has focus,
and Shift+F10 to open context menus normally accessible with a right-click. Since Surge XT is a very complex application with many controls,
you will also find the Alt+Period/Comma shortcuts to jump between the major sections very helpful.

If you wish to explore the screen in more detail without moving the system focus, all widely adopted Windows screen readers offer some way of
exploring the screen using a hierarchical approach (much like how VoiceOver works on macOS) and you can use these deeper navigation features to
jump from group to group in Surge.
We've put together some hints for hierarchical navigation with the three most common Windows screen readers below. For full details of these features, please refer to their respective documentation.


#### NVDA

NVDA’s review feature is called the Object Navigator. It can be moved around using the NVDA key in combination with the numpad,
or the arrow keys if you’re using NVDA's laptop layout. The most important keys you’ll need to know are:

- Move to the previous or next control in the current group: NVDA+Numpad4 or Numpad6 (desktop), NVDA+Shift+Left or Right (laptop)
- Move into or out of a group: NVDA+Numpad2 or Numpad8 (desktop), NVDA+Shift+Down or Up (laptop)
- Activate the control under the navigator: NVDA+Numpad Enter (desktop), NVDA+Enter (laptop). Use this to click buttons, toggle checkboxes etc.
- Set the system focus to the navigator: NVDA+Numpad Minus (desktop), NVDA+Shift+Backspace (laptop).
Use this to focus a slider for further adjustment using arrow keys, Home, End, Delete etc.

Also, if using Surge XT in combination with REAPER you find that NVDA takes a few seconds to respond when exiting menus, telling REAPER to run Surge XT in a dedicated process may help. To do this, after you find Surge XT in the add FX dialog, bring up the context menu and select **Run as > Dedicated process**. You should need to do this only once.


#### Narrator

The Narrator cursor performs similarly to NVDA’s Object Navigator. However, at default settings, it moves through controls sequentially,
ignoring grouping information. This can be changed by going into Narrator’s settings (Control+Windows+N) and changing the "Navigation mode"
combo box from "Basic" to "Advanced".
In Advanced mode, Narrator+Left or Right moves between controls within the current group as usual, Control+Narrator+Down or Up moves in and out of groups, and Narrator+Enter activates controls.
 
Narrator synchronizes the system focus automatically, so there's no need to manually route focus for further adjustment using Surge XT's native keystrokes.

Narrator includes a Find feature which can be used to jump to a specific control. You can access this by pressing Control+Narrator+F, typing in part of the name of the control you want to jump to, then hitting Enter.


#### JAWS

The JAWS touch cursor can be activated by pressing Shift+Numpad Plus on desktop layout, or JAWS+Shift+Semicolon on laptop layout.
At default settings, touch cursor ignores grouping, but this can be changed by pressing Numpad Star or JAWS+A.
Once done, Left and Right arrows move through controls within a group, Down and Up arrows move into and out of groups, and Enter activates controls.
You can return the arrow keys to normal operation by switching back to PC cursor (Numpad Plus on desktop, or JAWS+Semicolon twice quickly on laptop)
