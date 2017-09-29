# NAME

Emoji::NationalFlag - convert from country code to national flag emoji

# SYNOPSIS

    use Emoji::NationalFlag qw/ code2flag flag2code /;
    use utf8;

    is code2flag('jp'), "🇯🇵";
    is code2flag('jp'), "\x{1F1EF}\x{1F1f5}";

    is flag2code("🇯🇵"), 'jp';
    is flag2code("\x{1F1EF}\x{1F1f5}"), 'jp';

# DESCRIPTION

Emoji::NationalFlag is a module to convert from country code (ISO 3166-1 alpha-2) to national flag emoji, and vice versa

# METHODS

## code2flag($iso\_3166\_1\_alpha\_2\_code): Optional\[NationalFlagEmoji\]

This method returns national flag emoji if the supplied code (case insensitive) is valid, otherwise returns `undef`

## flag2code($decoded\_national\_flag\_emoji): Optional\[lc(CountryCodeAlpha-2)\]

This method returns lower case of ISO 3166-1 alpha-2 country code if the supplied emoji is valid, otherwise returns `undef`

# AUTHOR

punytan <punytan@gmail.com>

# COPYRIGHT

Copyright 2017- punytan

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO
