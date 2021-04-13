<h1 align="center">Birthdays Dwains Dashboard Add-on (more_page)</h1>

<p align="center">
  <a href="https://dwainscheeren.github.io/dwains-lovelace-dashboard/">
    <img src="https://img.shields.io/badge/Dwains%20Dashboard-Default-orange.svg" />
  </a>
  <a href="https://github.com/custom-components/hacs">
    <img src="https://img.shields.io/badge/HACS-Default-orange.svg" />
  </a>
  <a href="https://github.com/LRvdLinden/LRvdLinden/birthdays_dd_addon">
    <img src="https://img.shields.io/github/v/release/LRvdLinden/LRvdLinden/birthdays_dd_addon" />
  </a>
  <a href="https://github.com/LRvdLinden/LRvdLinden/birthdays_dd_addon">
    <img src="https://img.shields.io/github/commit-activity/m/LRvdLinden/LRvdLinden/birthdays_dd_addon" />
  </a>
</p>

<p align="center">Present Birtdays in a nice way.</p>

<p align="center">Created by <a href="https://github.com/LRvdLinden">Léon van der Linden</a>
</p> 


![uptimerobot](https://www.iphonelife.com/sites/iphonelife.com/files/memoji_0.jpg)

### Prerequisite
- Make sure you have the [Google Calendar Event](https://www.home-assistant.io/integrations/calendar.google/) integration
```yaml
     # Example configuration.yaml entry
     google:
       client_id: YOUR_CLIENT_ID
       client_secret: YOUR_CLIENT_SECRET
```
- Make a calendar in Google with all the birthdays and sync the calendar with Home Assistant
- Make sure you have installed [fontawesome icons](https://github.com/thomasloven/hass-fontawesome). This can be done manually or directly via hacs.

### Installation Add-on
- Copy the `birthdays` folder in to the `dwains-dashboard/addons/more_page` directory.
- Open your `more_page.yaml` file in `dwains-dashboard/configs` and add the following;
 ```yaml
     - name: Birthdays
       main_menu: 'true' #Show this addon in the main navigation bar!
       icon: fas:gifts
       path: 'dwains-dashboard/addons/more_page/birthdays/page.yaml'
```
- Reload the theme configuration via Theme Settings

### Replace the following
 ```yaml
            - type: custom:atomic-calendar-revive
              style: |
                ha-card {
                  border-radius: 5px;
                  background-color: var(--dwains-theme-primary);
                }
                .cal-titleContainer {
                  display: none;
                }
              showProgressBar: false
              eventBarColor: 'var(--dwains-theme-grey)'
              dayWrapperLineColor: 'var(--dwains-theme-grey)'
              timeColor: 'var(--dwains-theme-grey)'
              entities:
                - calendar.friends_birthdays
```
- on line 60: add the correct `entity` or `entities` to show


### Result

![IMG_0544](https://user-images.githubusercontent.com/77990847/114402640-52bd1f80-9ba4-11eb-990e-7a04642bd641.PNG)
