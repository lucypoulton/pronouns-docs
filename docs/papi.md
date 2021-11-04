## Placeholders

When running on Bukkit, ProNouns provides a number of 
[PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) placeholders:

- `%pronouns_pronouns%` - Nicely displays pronouns, for example She/Her, He/They, Any, Unset etc
- `%pronouns_all%` - displays the primary pronoun set in its canonical format (see [Formats](formats.md))

The following 6 placeholders refer to specific forms of pronouns (see [Formats](formats.md) for more info):

- `%pronouns_objective%` 
- `%pronouns_subjective%`
- `%pronouns_progressive%`
- `%pronouns_possessiveadj%`
- `%pronouns_possessivepro%`
- `%pronouns_reflexive%`
 
Placeholders can be appended with the following modifiers to control the output format:

- `upper` - MAKES EVERYTHING UPPERCASE
- `lower` - makes everything lowercase
- `capital` - Makes Everything Capital
- `nounset` (for `pronouns` placeholder only) - instead of displaying "unset", 
do not display anything if the player has not set their pronouns. 

Some examples:

- `%pronouns_subjective_upper%` - SHE
- `%pronoun_possessivepro_capital%` - Hers
