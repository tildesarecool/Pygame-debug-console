# Pygame debug console
My attempt at a pygame debug console for future use

My first task turned out to be unrelated: use hex representations of RGB rather decimal.

Turns out it wasn't very hard:

```Python
def colorHexToDec(hex_color) -> str:
    red = int(hex_color[0:2], 16)
    green = int(hex_color[2:4], 16)
    blue = int(hex_color[4:6], 16)      
    return red, green, blue

```

Now in pygame I can do something like this:

```Python
# Example usage of colorHexToDec
color = colorHexToDec("ffff00")

# Draw a rectangle with the color
pygame.draw.rect(screen, color, (100, 100, 200, 150))
```

And why, you ask, would I possibly want to do this?

Well, I have this color chart left over from a long lost copy of that famous HTML 5 book that ran for like 20 years and had 12 or whatever editions to it...anyway in the back of every copy was this fold out full color chart with the hex representations of a bunch colors and the actual colors (in color).

So I've pinned it above my desk and plan on using it for randomly choosing colors. Seems like the long way round just for some colors maybe, but at least it wasn't very hard.
