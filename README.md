BitFieldDraw
============

"Bit Field Drawings" are 2D drawings generated from simple functions for digital art.

Example Code
------------

    >>> import bitfielddraw
    >>> # Draw the bitfield on the screen:
    >>> bitfielddraw.printBitFieldStr(lambda x, y: (x^y)%5, width=20, height=20)
    ██████▀▄██▄▀▀▄████▀▄
    ████▀▄██▄▀████▀▄▀▄██
    ▄▀██▀▄████▄▀██▀▄▀▄██
    ██▄▀██▀▄▄▀██▀▄████▀▄
    ▀▄██▄▀████▀▄██▄▀██▄▀
    ██▀▄██▄▀▀▄██▄▀██▄▀██
    ██▄▀██▀▄▄▀██▀▄████▀▄
    ▄▀██▀▄████▄▀██▀▄▀▄██
    ██▀▄██▄▀▀▄██▄▀██████
    ▀▄██▄▀████▀▄██▄▀████
    >>> bitfielddraw.printBitFieldStr(lambda x, y: (x^y)%5, invertBit=True, width=20, height=20)
          ▄▀  ▀▄▄▀    ▄▀
        ▄▀  ▀▄    ▄▀▄▀
    ▀▄  ▄▀    ▀▄  ▄▀▄▀
      ▀▄  ▄▀▀▄  ▄▀    ▄▀
    ▄▀  ▀▄    ▄▀  ▀▄  ▀▄
      ▄▀  ▀▄▄▀  ▀▄  ▀▄
      ▀▄  ▄▀▀▄  ▄▀    ▄▀
    ▀▄  ▄▀    ▀▄  ▄▀▄▀
      ▄▀  ▀▄▄▀  ▀▄
    ▄▀  ▀▄    ▄▀  ▀▄
    >>> bitfielddraw.getBitFieldStr(lambda x, y: (x^y)%5, invertBit=True, width=20, height=20)
    '      ▄▀  ▀▄▄▀    ▄▀\n    ▄▀  ▀▄    ▄▀▄▀  \n▀▄  ▄▀    ▀▄  ▄▀▄▀  \n  ▀▄  ▄▀▀▄  ▄▀    ▄▀\n▄▀  ▀▄    ▄▀  ▀▄  ▀▄\n  ▄▀  ▀▄▄▀  ▀▄  ▀▄  \n  ▀▄  ▄▀▀▄  ▄▀    ▄▀\n▀▄  ▄▀    ▀▄  ▄▀▄▀  \n  ▄▀  ▀▄▄▀  ▀▄      \n▄▀  ▀▄    ▄▀  ▀▄    '

    >>> # Save the bit field to a PNG image file:
    >>> im = bitfielddraw.getBitFieldImg(lambda x, y: (x^y)%5, invertBit=True, width=20, height=20)
    >>> im.save('output.png')


    >>> bitfielddraw.getBitField(lambda x, y: (x^y)%5, width=20, height=20)
    frozenset({(7, 17), (18, 17), (8, 0), (19, 0), (8, 9), (19, 9), (11, 5), (8, 18), (19, 18), (0, 14), (4, 2), (3, 15), (14, 15), (15, 7), (7, 3), (18, 3), (15, 16), (7, 12), (8, 4), (19, 4), (11, 0), (0, 9), (11, 9), (3, 1), (3, 10), (14, 10), (3, 19), (14, 19), (15, 2), (15, 11), (18, 7), (7, 16), (18, 16), (10, 8), (10, 17), (3, 5), (14, 5), (3, 14), (15, 6), (18, 2), (7, 11), (6, 15), (10, 3), (10, 12), (2, 17), (3, 0), (14, 0), (14, 9), (3, 18), (14, 18), (6, 10), (6, 19), (10, 7), (2, 3), (10, 16), (2, 12), (3, 4), (17, 6), (9, 11), (6, 5), (6, 14), (10, 2), (10, 11), (2, 16), (16, 18), (17, 1), (5, 8), (17, 10), (17, 19), (9, 15), (6, 0), (10, 6), (2, 11), (1, 15), (13, 17), (16, 13), (5, 3), (9, 1), (5, 12), (17, 14), (9, 10), (9, 19), (6, 4), (6, 13), (13, 3), (1, 10), (13, 12), (16, 8), (1, 19), (16, 17), (17, 0), (5, 7), (17, 9), (9, 5), (5, 16), (9, 14), (12, 15), (1, 5), (16, 3), (13, 16), (16, 12), (5, 2), (17, 4), (9, 0), (5, 11), (0, 18), (12, 1), (12, 10), (4, 6), (12, 19), (4, 15), (1, 0), (1, 9), (13, 11), (16, 7), (1, 18), (5, 6), (19, 8), (0, 4), (19, 17), (0, 13), (11, 13), (12, 5), (12, 14), (4, 10), (4, 19), (16, 2), (1, 13), (8, 3), (19, 3), (19, 12), (8, 12), (0, 8), (11, 8), (0, 17), (11, 17), (12, 0), (4, 5), (15, 1), (7, 6), (15, 19), (7, 15), (18, 15), (0, 3), (11, 3), (19, 16), (8, 16), (0, 12), (11, 12), (12, 4), (4, 0), (4, 9), (3, 13), (14, 13), (7, 1), (18, 1), (15, 14), (7, 10), (18, 10), (18, 19), (19, 2), (8, 11), (19, 11), (0, 7), (11, 7), (0, 16), (11, 16), (3, 8), (14, 8), (3, 17), (14, 17), (15, 9), (7, 5), (18, 5), (15, 18), (7, 14), (18, 14), (19, 6), (0, 2), (11, 2), (14, 3), (14, 12), (15, 4), (7, 0), (18, 0), (15, 13), (7, 9), (18, 9), (10, 1), (2, 6), (2, 15), (3, 7), (14, 7), (3, 16), (17, 18), (7, 4), (18, 4), (6, 8), (6, 17), (2, 1), (10, 14), (2, 10), (2, 19), (3, 2), (14, 2), (3, 11), (17, 13), (9, 18), (10, 9), (2, 5), (10, 18), (2, 14), (14, 6), (9, 4), (9, 13), (6, 7), (6, 16), (10, 4), (2, 0), (10, 13), (2, 9), (13, 6), (2, 18), (13, 15), (16, 11), (5, 1), (17, 3), (17, 12), (9, 8), (5, 19), (9, 17), (6, 2), (6, 11), (2, 4), (13, 1), (1, 8), (13, 10), (16, 6), (1, 17), (16, 15), (17, 7), (5, 14), (17, 16), (12, 13), (4, 18), (1, 3), (13, 5), (16, 1), (1, 12), (13, 14), (16, 10), (16, 19), (17, 2), (5, 9), (17, 11), (9, 7), (5, 18), (6, 1), (12, 8), (12, 17), (4, 13), (13, 0), (1, 7), (13, 9), (16, 5), (1, 16), (13, 18), (5, 4), (9, 2), (5, 13), (8, 6), (8, 15), (19, 15), (0, 11), (4, 8), (4, 17), (1, 2), (13, 4), (16, 0), (7, 18), (8, 1), (19, 1), (8, 10), (0, 6), (11, 6), (8, 19), (11, 15), (12, 7), (4, 3), (12, 16), (4, 12), (1, 6), (15, 8), (18, 13), (8, 5), (19, 5), (0, 1), (8, 14), (19, 14), (11, 10), (0, 19), (11, 19), (12, 2), (12, 11), (4, 7), (15, 3), (15, 12), (18, 8)})

Example Art
------------

    >>> printBitFieldStr(lambda x, y: (x ^ y) % 5)
    ██████▀▄▀▄██▄▀████▀▄██▄▀▄▀████████▄▀▀▄████████▀▄▀▄██▄▀████▀▄██▄▀██▀▄██▄▀▄▀████████▄▀▀
    ████▀▄████▀▄██▄▀▀▄██▄▀████▄▀████▄▀████▀▄████▀▄████▀▄██▄▀▀▄██▄▀██▀▄██▄▀████▄▀████▄▀███
    ▄▀██▀▄████▀▄████████▄▀████▄▀██▀▄██▀▄████▀▄████▄▀██▄▀██▀▄▄▀██▀▄██████▄▀████▄▀██▀▄██▀▄█
    ██▄▀██▀▄▀▄████████████▄▀▄▀██▀▄██▀▄████████▀▄▄▀██▄▀██▀▄████▄▀██▀▄██████▄▀▄▀██▀▄██▀▄███
    ▀▄██▄▀████████▀▄▄▀████████▀▄██▄▀██████▀▄██▄▀▀▄████▀▄██▄▀▀▄██▄▀██▄▀████████▀▄██▄▀█████
    ██▀▄██▄▀████▀▄████▄▀████▀▄██▄▀██████▀▄██▄▀████▀▄▀▄██▄▀████▀▄██▄▀██▄▀████▀▄██▄▀██████▀
    ██▄▀██▀▄████▄▀████▀▄████▄▀██▀▄██▄▀██▀▄████▄▀██▀▄▀▄████▄▀██▀▄████▀▄████▄▀██▀▄██████▄▀█
    ▄▀██▀▄████████▄▀▀▄████████▄▀██▀▄██▄▀██▀▄▄▀██▀▄████▀▄▄▀██▀▄████████▀▄▄▀██▀▄██████▄▀██▀
    ██▀▄██▄▀▄▀████████████▀▄▀▄██▄▀██▀▄██▄▀████▀▄██▄▀██▄▀▀▄████████▀▄██▄▀▀▄████████▀▄██▀▄█
    ▀▄██▄▀████▄▀████████▀▄████▀▄██▄▀██▀▄██▄▀▀▄██▄▀██▄▀████▀▄████▀▄██▄▀████▀▄████▀▄██▀▄██▄
    ████▄▀████▄▀██▀▄▄▀██▀▄████▀▄██████▄▀██▀▄▄▀██▀▄████▀▄████▀▄████▄▀██▀▄████▀▄████▄▀████▄
    ██████▄▀▄▀██▀▄████▄▀██▀▄▀▄██████▄▀██▀▄████▄▀██▀▄▀▄████████▀▄▄▀██▀▄████████▀▄▄▀███████
    ▄▀████████▀▄██▄▀▀▄██▄▀████████▀▄██▀▄██▄▀▀▄██▄▀████████▀▄██▄▀▀▄████████▀▄██▄▀▀▄██▄▀███
    ██▄▀████▀▄██▄▀████▀▄██▄▀████▀▄██▀▄██▄▀████▀▄██▄▀████▀▄██▄▀████▀▄████▀▄██▄▀████▀▄██▄▀█
    ▀▄████▄▀██▀▄████▄▀██▀▄████▄▀██▀▄██▀▄████▄▀██▀▄████▄▀██▀▄████▄▀██▄▀██▀▄████▄▀██▀▄████▄
    ██▀▄▄▀██▀▄████████▄▀██▀▄▄▀██▀▄██▀▄████████▄▀██▀▄▄▀██▀▄████████▄▀██▄▀██▀▄▄▀██▀▄███████
    ██▄▀▀▄████████▀▄▀▄██▄▀████▀▄██▄▀██████▀▄▀▄██▄▀████▀▄██▄▀▄▀██████▀▄██▄▀████▀▄██▄▀▄▀███
    ▄▀████▀▄████▀▄████▀▄██▄▀▀▄██▄▀██████▀▄████▀▄██▄▀▀▄██▄▀████▄▀██████▀▄██▄▀▀▄██▄▀████▄▀█
    ██▀▄████▀▄████▄▀██▄▀██▀▄▄▀██▀▄██▄▀██▀▄████▀▄████████▄▀████▄▀██▀▄██▄▀██▀▄▄▀██▀▄██▀▄███
    ▀▄████████▀▄▄▀██▄▀██▀▄████▄▀██▀▄██▄▀██▀▄▀▄████████████▄▀▄▀██▀▄██▄▀██▀▄████▄▀██▀▄██▀▄▄
    ██████▀▄██▄▀▀▄████▀▄██▄▀▀▄██▄▀██▀▄██▄▀████████▀▄▄▀████████▀▄██▄▀██▀▄██▄▀▀▄██▄▀████▄▀▀
    ████▀▄██▄▀████▀▄▀▄██▄▀████▀▄██▄▀██▀▄██▄▀████▀▄████▄▀████▀▄██▄▀██▀▄██▄▀████▀▄██▄▀▄▀███
    ▄▀██▀▄████▄▀██▀▄▀▄████▄▀██▀▄██████▄▀██▀▄████▄▀████▀▄████▄▀██▀▄██████▄▀██▀▄████▄▀▄▀██▀
    ██▄▀██▀▄▄▀██▀▄████▀▄▄▀██▀▄██████▄▀██▀▄████████▄▀▀▄████████▄▀██▀▄██████▄▀██▀▄▄▀████▄▀█
    ▀▄██▄▀████▀▄██▄▀██▄▀▀▄████████▀▄██▀▄██▄▀▄▀████████████▀▄▀▄██▄▀██▄▀████████▄▀▀▄██▀▄██▄
    ██▀▄██▄▀▀▄██▄▀██▄▀████▀▄████▀▄██▀▄██▄▀████▄▀████████▀▄████▀▄██▄▀██▄▀████▄▀████▀▄██▀▄█
    ██▄▀██▀▄▄▀██▀▄████▀▄████▀▄████▄▀████▄▀████▄▀██▀▄▄▀██▀▄████▀▄████▀▄████▄▀████▄▀████▄▀█
    ▄▀██▀▄████▄▀██▀▄▀▄████████▀▄▄▀████████▄▀▄▀██▀▄████▄▀██▀▄▀▄████████▀▄▄▀████████▄▀▄▀██▀
    ██▀▄██▄▀▀▄██▄▀████████▀▄██▄▀▀▄██▄▀████████▀▄██▄▀▀▄██▄▀████████▀▄██▄▀▀▄██▄▀████████▀▄█
    ▀▄██▄▀████▀▄██▄▀████▀▄██▄▀████▀▄██▄▀████▀▄██▄▀████▀▄██▄▀████▀▄██▄▀████▀▄██▄▀████▀▄██▄

    >>> printBitFieldStr(lambda x, y: (x | y) % 7)
    ████▄ ▄ ████▄ ▄ ████▄ ▄ ████▄ ▄ ████▄ ▄ ████▄ ▄ ████▄ ▄ ████▄ ▄ ████▀█▀█████▀█▀█████▀
    ▀█████▄ ▀█████▄ ▀█████▄ ▀█████▄ ▀█████▄ ▀█████▄ ▀█████▄ ▀█████▄ ██████▀███████▀██████
    ████████▄ ▄ ▄ ▄ ████████▄ ▄ ▄ ▄ ████████▄ ▄ ▄ ▄ ████████▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ▀█▀█▀█▀█▄ ▄ ▄
    ██████████▄ ██▄ ██████████▄ ██▄ ██████████▄ ██▄ ██████████▄ ██▄ ██▄ ██▄ ██▀███▀███▄ █
    ████████████▄ ▄ ████████████▄ ▄ ████████████▄ ▄ ████████████▄ ▄ ████▄ ▄ ████▀█▀█████▄
    ▄ ██████▀█████▄ ▄ ██████▀█████▄ ▄ ██████▀█████▄ ▄ ██████▀█████▄ ▀█████▄ ██████▀█▀████
    ████████████████▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ████████████████▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ████████████████▀█▀█▀
    ██████████████████▄ ██▄ ██▄ ██▄ ██████████████████▄ ██▄ ██▄ ██▄ ██████████████████▀██
    ▀█▀█████▀█▀█████████▄ ▄ ████▄ ▄ ▀█▀█████▀█▀█████████▄ ▄ ████▄ ▄ ████████████████████▀
    ██▀███████▀█████▀█████▄ ▀█████▄ ██▀███████▀█████▀█████▄ ▀█████▄ ▄ ██████▄ ███████████
    ████████████████████████▄ ▄ ▄ ▄ ████████████████████████▄ ▄ ▄ ▄ ████████████████▄ ▄ ▄
    ██████████████████████████▄ ██▄ ██████████████████████████▄ ██▄ ██████████████████▄ █
    ▄ ▄ ████▀█▀█████████████████▄ ▄ ▄ ▄ ████▀█▀█████████████████▄ ▄ ▀█▀█████████████████▄
    ██▄ ██████▀█████▄ ██████▀█████▄ ██▄ ██████▀█████▄ ██████▀█████▄ ██▀█████▄ ██████▀████
    ████████████████████████████████▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ █████████████████████
    ▀███▀███▀███▀███▀███▀███▀███▀█████▄ ██▄ ██▄ ██▄ ██▄ ██▄ ██▄ ██▄ █████████████████████
    ████████████████████████████████████▄ ▄ ████▄ ▄ ████▄ ▄ ████▄ ▄ ▄ ▄ ████▄ ▄ ████▄ ▄ █
    ████▀███████▀███████▀███████▀███▀█████▄ ▀█████▄ ▀█████▄ ▀█████▄ ██▄ ██████▄ ██████▄ █
    ████████████████████████████████████████▄ ▄ ▄ ▄ ████████▄ ▄ ▄ ▄ █████████████████████
    ▄ ██▄ ██▀███▀███▄ ██▄ ██▀███▀█████████████▄ ██▄ ██████████▄ ██▄ ▀███▀███████████▀███▀
    ████████████████████████████████████████████▄ ▄ ████████████▄ ▄ ████████▄ ▄ █████████
    ████▄ ██████▀███████▄ ██████▀███▄ ██████▀█████▄ ▄ ██████▀█████▄ ████▀█████▄ ████████▀
    ▀█▀█▀█▀█▀█▀█▀█▀█████████████████████████████████▄ ▄ ▄ ▄ ▄ ▄ ▄ ▄ █████████████████████
    ██▀███▀███▀███▀█▀███▀███▀███▀█████████████████████▄ ██▄ ██▄ ██▄ ▄ ██▄ ██▄ ██▄ ███████
    ████▀█▀█████▀█▀█████████████████▀█▀█████▀█▀█████████▄ ▄ ████▄ ▄ ████████████████▄ ▄ █
    ██████▀███████▀█████▀███████▀█████▀███████▀█████▀█████▄ ▀█████▄ ████▄ ██████▄ ████▄ █
    ▄ ▄ ▄ ▄ ▀█▀█▀█▀█████████████████████████████████████████▄ ▄ ▄ ▄ ▀█▀█▀█▀██████████████
    ██▄ ██▄ ██▀███▀█▄ ██▄ ██▀███▀█████████████████████████████▄ ██▄ ██▀███▀█▄ ██▄ ██▀███▀
    ████▄ ▄ ████▀█▀█████████████████▄ ▄ ████▀█▀█████████████████▄ ▄ ████▀█▀██████████████
    ▀█████▄ ██████▀█████▄ ██████▀█████▄ ██████▀█████▄ ██████▀█████▄ ██████▀█████▄ ██████▀

    >>> printBitFieldStr(lambda x, y: (x * 64) % y)
     ████████████████████████████▀████████████████████████████▀▄█████████████████████████
     ██████▀██████▀██████▀██████▀██████▀██████▀██████▀██████▀▄█████▀██████▀██████▀██████▀
     ██████████████████████████▀██████████████████████████▀▄█████████████████████████▀███
     ████████████▀████████████▀████████████▀████████████▀▄███████████▀████████████▀██████
     ████████████████████████▀████████████████████████▀▄███████████████████████▀█████████
     ██▀██▀██▀██▀██▀██▀██▀██▀██▀██▀██▀██▀██▀██▀██▀██▀▄█▀██▀██▀██▀██▀██▀██▀██▀██▀██▀██▀██▀
     ██████████████████████▀██████████████████████▀▄█████████████████████▀███████████████
     ██████████▀██████████▀██████████▀██████████▀▄█████████▀██████████▀██████████▀███████
     ████████████████████▀████████████████████▀▄███████████████████▀████████████████████▀
     ████▀████▀████▀████▀████▀████▀████▀████▀▄███▀████▀████▀████▀████▀████▀████▀████▀█▄██
     ██████████████████▀██████████████████▀▄█████████████████▀██████████████████▀█▄██████
     ████████▀████████▀████████▀████████▀▄███████▀████████▀████████▀████████▀█▄██████▀███
     ████████████████▀████████████████▀▄███████████████▀████████████████▀█▄██████████████
     ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀
     ██████████████▀██████████████▀▄█████████████▀██████████████▀█▄████████████▀█████████
     ██████▀██████▀██████▀██████▀▄█████▀██████▀██████▀██████▀█▄████▀██████▀██████▀██████▀
     ████████████▀████████████▀▄███████████▀████████████▀█▄██████████▀████████████▀██▄███
     ██▀██▀██▀██▀██▀██▀██▀██▀▄█▀██▀██▀██▀██▀██▀██▀██▀█▄▀██▀██▀██▀██▀██▀██▀██▀██ ██▀██▀██▀
     ██████████▀██████████▀▄█████████▀██████████▀█▄████████▀██████████▀██▄███████▀███████
     ████▀████▀████▀████▀▄███▀████▀████▀████▀█▄██▀████▀████▀████▀██▄█▀████▀████▀████▀███▄
     ████████▀████████▀▄███████▀████████▀█▄██████▀████████▀██▄█████▀████████▀███▄████▀███
     ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀
     ██████▀██████▀▄█████▀██████▀█▄████▀██████▀██▄███▀██████▀███▄██▀██████▀████▄█▀██████▀
     ██▀██▀██▀██▀▄█▀██▀██▀██▀█▄▀██▀██▀██▀██ ██▀██▀██▀██▀▄█▀██▀██▀██▀█▄▀██▀██▀██▀██ ██▀██▀
     ████▀████▀▄███▀████▀█▄██▀████▀██▄█▀████▀███▄▀████▀████ ████▀████▀▄███▀████▀█▄██▀████
     ▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀ ▀▀▀▀▀▀▀▀ ▀▀▀
     ██▀██▀▄█▀██▀█▄▀██▀██ ██▀██▀▄█▀██▀█▄▀██▀██ ██▀██▀▄█▀██▀█▄▀██▀██ ██▀██▀▄█▀██▀█▄▀██▀██
     ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀
     ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀ ▀▀

    >>> printBitFieldStr(lambda x, y: (x % y) % 4)
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄█
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄█
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄█
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄█
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▀
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▄█▀
     ███ ███ ███ ███ ███ ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▀█▄█▀█▄█▀
     ███ ███ ███ ███ ███ ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▄█▀█▄█▀█▄█▀
     ███ ███ ███ ███ ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▀█▄█▀█▄█▀█▄█▀█▄█▀
     ███ ███ ███ ███ ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▄█▀█▄█▀█▄█▀█▄█▀█▄█▀
     ███ ███ ███ ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▀█▄█▀█▄█▀█▄█▀█▄█▀█▄█▀█▄█▀
     ███ ███ ███ ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▄█▀█▄█▀█▄█▀█▄█▀█▄█▀█▄█▀█▄█▀
     ███ ███ ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▀█▄█▀█▄█▀█▄█▀█▄█▀█▄█▀█▄█▀█ ██▄▀██
     ███ ███ ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▄█▀█▄█▀█▄█▀█▄█▀█▄█▀█▄█▀█▄▄▀██▄▀██▄▀
     ███ ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄██▀▄▀█▄█▀█▄█▀█▄█▀█▄█▀█▄█▀█ ██▄▀██▄▀██▄▀██▄▀██
     ███ ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄██▀▄▄█▀█▄█▀█▄█▀█▄█▀█▄█▀█▄▄▀██▄▀██▄▀██▄▀██▄▀██▄
     ███ ███ ███ ███ █▀▄██▀▄██▀▄██▀▄██▀▄▀█▄█▀█▄█▀█▄█▀█▄█▀█ ██▄▀██▄▀██▄▀██▄▀█▀▄██ ███ ███
     ███ ███ ███ ███ ▄██▀▄██▀▄██▀▄██▀▄▄█▀█▄█▀█▄█▀█▄█▀█▄▄▀██▄▀██▄▀██▄▀██▄ ███ ███ ███ ███
     ███ ███ ███ █▀▄██▀▄██▀▄██▀▄▀█▄█▀█▄█▀█▄█▀█ ██▄▀██▄▀██▄▀█▀▄██ ███ ███ █▀█▄█▀▄██▀▄██▀▄▀
     ███ ███ ███ ▄██▀▄██▀▄██▀▄▄█▀█▄█▀█▄█▀█▄▄▀██▄▀██▄▀██▄ ███ ███ ███ ▄██▀▄██▀▄██▀▄▄█▀█▄█▀
     ███ ███ █▀▄██▀▄██▀▄▀█▄█▀█▄█▀█ ██▄▀██▄▀█▀▄██ ███ █▀█▄█▀▄██▀▄▀██▄▀█▄█▀█ ███ ██▄▀█▀▄██▀
     ███ ███ ▄██▀▄██▀▄▄█▀█▄█▀█▄▄▀██▄▀██▄ ███ ███ ▄██▀▄██▀▄▄█▀█▄█▀█▄▄▀██▄▀██▄ ███ ███ ▄██▀
     ███ █▀▄██▀▄▀█▄█▀█ ██▄▀█▀▄██ █▀█▄█▀▄▀██▄▀█ ███ █▀▄██▀▄▀█▄█▀█ ██▄▀█▀▄██ █▀█▄█▀▄▀██▄▀█
     ███ ▄██▀▄▄█▀█▄▄▀██▄ ███ ▄██▀▄▄█▀█▄▄▀██▄ ███ ▄██▀▄▄█▀█▄▄▀██▄ ███ ▄██▀▄▄█▀█▄▄▀██▄ ███
     █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█ █▀▄▀█



Reference
----------

TODO - finish this section

    getBitField(func, invertBit=False, left=0, bottom=0, width=None, height=None)

    getBitFieldImg(func, invertBit=False, left=0, bottom=0, width=None, height=None, trueColor='white', falseColor='black')

    saveBitFiledImg(filename, func, invertBit=False, left=0, bottom=0, width=None, height=None, trueColor='white', falseColor='black')

    getBitFieldStr(func, invertBit=False, left=0, bottom=0, width=None, height=None)

    printBitFieldStr(func, invertBit=False, left=0, bottom=0, width=None, height=None)

    saveBitFieldStr(filename, func, invertBit=False, left=0, bottom=0, width=None, height=None)

