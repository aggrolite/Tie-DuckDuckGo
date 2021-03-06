# NAME

Tie::DuckDuckGo - Access DuckDuckGo search results via variables

# SYNOPSIS

    use Tie::DuckDuckGo;

    # tie a scalar
    my $search;
    tie $search => 'Tie::DuckDuckGo' => 'perl';

    say $search->{url};
    say $search->{title};
    say $search->{snippet};

    # tie an array
    my @results;
    tie @results => 'Tie::DuckDuckGo' => 'perl';

    for (@results) {
      say $_->{url};
      say $_->{title};
      say $_->{snippet};
    }

    # tie a hash
    my %results;
    tie %results => 'Tie::DuckDuckGo';

    my $result = $results{reddit};
    say $_->{url} for @$result;

# DESCRIPTION

I came across Darren Chamberlain's neat implementation of [Tie::Google](https://metacpan.org/pod/Tie::Google) and
though it would be fun to write a version for DuckDuckGo.

I haven't implemented all of the require methods for tie(). I plan to add those
in a future release.

# AUTHOR

Curtis Brandt <curtis@cpan.org>

# COPYRIGHT

Copyright 2014- Curtis Brandt

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO

[Tie::Google](https://metacpan.org/pod/Tie::Google)
