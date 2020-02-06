# Cache

### Types of Cache Miss

- Compuilsory miss
- Capacity miss
- Conflict miss

### Direct-mapped Cache

- Cache index = (address in main memory) mod (number of cahe blocks)

### Fully associative Cache

- No cache index
- No conflict miss
- But too expensive
  - Too large MUX need

### N-way Set-associative Cache

- SOTA (at least for now)
- Cache index = (address in main memory) mod (number of sets)
- Number of rows = number of sets(lines)
- Number of columns = number of ways
- Set size = number of ways = set associativity
- Needs "replacement policy" when evicting its contents
  - Oracle policy
    - Sees the future
    - Impossible
  - LRU algorithm
    - Evict the line that was used least recently, ie, furthest in the past
    - Works well in practice
    - Require complex logic to keep track of ordering
    - Bad when working set becomes larger than cache size
  - Random
  - FIFO
  - Most Recently Used algorithm

### How much associativity/size?

- Application dependent

### Performance Improvement with Caches

- Depends on CPI with cache, CPI without cache, and miss rate
