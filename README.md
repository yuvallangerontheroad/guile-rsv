# An RSV implementation in GNU Guile.

## IMPORTANT NOTICE: The code is only available on:

- https://codeberg.org/kakafarm/guile-rsv/
- https://kaka.farm/stagit/guile-rsv/log.html

## Description:

You can read more about it on the [RSV Specification][1] and watch the
demonstration on [Youtube][2].

Work in progress.  Things may change.  If you have any ideas,
recommendations, bug reports, criticisms - all will be happily
received on the #scheme channel on https://libera.chat/ where I go by
cow_2001.

## Commands:

Currently,

- rsv2csm takes RSV in stdin and outputs sexps into stdout.
- scm2rsv takes sexps in stdin and outputs RSV into stdout.

You run scm2rsv like so:

```
$ printf '(("moo" #f) (#f "poo"))' | ./scm2rsv | hexdump -C
00000000  6d 6f 6f ff fe ff fd fe  ff 70 6f 6f ff fd        |moo......poo..|
0000000e
```

And you run rsv2csm like so:

```
$ printf '(("moo" #f) (#f "poo"))' | ./scm2rsv | ./rsv2scm
(("moo" #f) (#f "poo"))
```

## Repositories:

Main repository is at [Codeberg.org][3].

### Mirrors:

- [Kaka Farm's Stagit][4]
- [Github][5].

## Copyright:

The [example RSV test files](./TestFiles/) came from [commit
74757d0ba08132a38943027d8d81fc41388e791e][6] of the "main" branch of
[Stenway][7]'s RSV-Specification Rosetta Stone repository, and were
release under the [MIT-0][8] license.  The exact copyright notice can
be found in the [LICENSE file](./TestFiles/LICENSE).

[1]: https://github.com/Stenway/RSV-Specification
[2]: https://www.youtube.com/watch?v=tb_70o6ohMA
[3]: https://codeberg.org/kakafarm/guile-rsv/
[4]: https://kaka.farm/stagit/guile-rsv/log.html
[5]: https://github.com/yuvallangerontheroad/guile-rsv
[6]: https://github.com/Stenway/RSV-Challenge/tree/74757d0ba08132a38943027d8d81fc41388e791e/TestFiles
[7]: https://www.stenway.com/
[8]: https://opensource.org/license/mit-0/
