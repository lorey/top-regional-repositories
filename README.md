![A map of Europe](.github/world.jpg)

# Top Regional Repositories

Want to explore repositories that are popular in a specific region, e.g. the city/country you live in? This project will help you. For many cities and all countries worldwide it lists the repositories with the highest ratio of stars from users in that region. See it as a list of the most-relevant repositories for a specific region.

## Cities you might be interested in

- [San Francisco](cities/united-states-san-francisco.md)
- [London](cities/united-kingdom-london.md)
- [Seattle](cities/united-states-seattle.md)
- [New York](cities/united-states-new-york.md)
- [Paris](cities/france-paris.md)
- [Beijing](cities/china-beijing.md)
- [Berlin](cities/germany-berlin.md)
- [Singapore](cities/singapore-singapore.md)
- [Austin](cities/united-states-austin.md)
- [Bengaluru](cities/india-bengaluru.md)

## Countries you might be interested in

- [United States](countries/united-states.md)
- [United Kingdom](countries/united-kingdom.md)
- [Germany](countries/germany.md)
- [France](countries/france.md)
- [China](countries/china.md)

## How it works

Basically, for each popular repository and a given region I compute the ratio of stars from users in the given region (stars from users inside region divided by overall stars). As this favors small repositories, I add 1000 to the number of stars to favor bigger repositories (a repo with three stars can otherwise get a ratio of 1 easily). This leads to a score defined as follows:

```
score(repo, region) := #(stars from users in the given region) / (#(stars of repo) + 1000)
```

To be able to compute the given score, I have used the geocoded locations of popular GitHub users. I know, this favors repositories starred by popular GitHub users, but I don't think the effect is statistically relevant. The small number of geocoded users should be a bigger problem for statistical correctness :)

## Find the best programmers worldwide

I have a project called Programmer Map where you can find [the best programmers as well as interesting repos for many cities worldwide](http://programmermap.com). This is a new feature and will be integrated soon.

Image: [TheAndrasBarta on Pixabay. CC0](https://pixabay.com/en/users/TheAndrasBarta-2004841/)
