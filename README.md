# Daily Color Palettes

Goal: Find a holiday/event color palette for every day of the year by language and location.

## Status

Started with US-based events.

## Data Format

Data is stored in YAML files. JSON is generated from the YAML after validation.

Fields:

```yaml
events:
  - name: Event Name
    description: One or more sentences describing the event.
    schedule: # Multiple types of schedules are allowed.
      # Specific Day
      month: 1 # Month Number (one indexed)
      day: 1 # Day Number
      # Floating Day
      month: 1 # Month Number (one indexed)
      weekday: Monday
      offset: 3 # 3rd Monday of the Month
      # Date Range
      range-date:
        - 03-01
        - 05-30
    colors: # Colors ordered by priority
      - colorname: ffffff # six character RGB HEX value
```

## TODO

- Add remaining holiday colors.
- Add `location:` and `country:` fields.
- Add localized holidays.
- Add country flags.
- Add sports teams and the Olympics.
- Daily Palette Lookup
  - https://github.com/rickar/cal
  - Lookup returns most specific palette for the day, sorted by day,
    floating-day, date-range, and default.
- Allow Color sub-palettes.
- Add "exact date" type, including year, for events with complex date
  calculations.
- Add events/holidays with complex dates:
  - Easter - Easter always falls on the first Sunday after the first full moon
    that occurs on or after the vernal equinox.
  - Ash Wednesday - 46 days before Easter.
  - Fat Tuesday - Day before Ash Wednesday.
  - Hanukkah - Right nights and days, starting on the 25th day of Kislev
    according to the Hebrew calendar.
  - Holi - Holi (also known as Phagwah or Bhojpuri) is celebrated on the Phalgun
    Purnima (or Pooranmashi, Full Moon) in the month of Phalgun.
