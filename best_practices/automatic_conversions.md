### Automatic Conversions
- Avoid automatic conversion where possible. 
- Single parameter constructors can be marked `explicit` to prevent the possibility of automatic conversion
  - Single parameter constructors provide automatic conversions.
- Automatic conversion can make unnecessary copies and increase overhead.
- Conversion operations should also be marked `explicit` to avoid accidental conversions. 
