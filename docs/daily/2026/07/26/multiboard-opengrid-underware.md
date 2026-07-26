# MultiBoard, openGrid and Underware

**Date:** 2026-07-26

> This page was created with the assistance of ChatGPT. Information should be verified before making design, printing or purchasing decisions.

This page compares MultiBoard and openGrid and explains how the Underware cable-management system relates to both platforms.

## Sources

The initial reference was a discussion on [Woodworking.nl](https://www.woodworking.nl/threads/multiboard-french-cleats-alternatief.45826/).

The discussion mentions MultiBoard as a possible 3D-printed alternative to pegboard or French-cleat storage. One participant used MultiBoard together with Underware for cable management and found that the system worked, but required considerable printing time and many small parts.

Relevant project pages include:

- [MultiBuild](https://multibuild.io/)
- [openGrid](https://www.opengrid.world/)
- [Underware 2.0 for MultiBoard](https://makerworld.com/nl/models/783010-underware-2-0-infinite-cable-management?appSharePlatform=copy#profileId-1504508)
- [Underware for openGrid](https://makerworld.com/en/models/1175037-underware-for-opengrid)

## Relationship

MultiBoard and openGrid are two separate mounting systems.

MultiBoard is part of the wider MultiBuild ecosystem:

```text
MultiBuild
├── MultiBoard
├── MultiBin
└── other related components
```

openGrid is an independent mounting framework:

```text
openGrid
├── Full boards
├── Lite boards
├── mounting snaps
├── accessory snaps
└── compatible accessories and adapters
```

Underware is not a third competing wall-grid system. It is a modular cable-management concept that can be adapted to different mounting platforms:

```text
Underware
├── Underware 2.0 for MultiBoard
└── Underware for openGrid
```

The cable-management principle is similar, but the physical connection to the board is specific to each mounting system.

## Shared Technical Principle

At a high level, MultiBoard and openGrid work in a similar way:

```text
printed base tiles
        ↓
tiles mounted to a wall, desk or frame
        ↓
accessories attached at repeated grid positions
```

Both systems allow a larger mounting surface to be assembled from multiple printed tiles.

Accessories can be removed, repositioned or replaced without rebuilding the complete installation.

They can both be used for purposes such as:

- Tool storage
- Shelves and holders
- Small containers
- Electronics mounting
- Desk organisation
- Cable management

The systems are therefore conceptually similar, but their grids and connector designs are different.

## Grid Dimensions

MultiBoard uses a 25 mm grid.

```text
MultiBoard grid spacing = 25 mm
```

openGrid uses a 28 mm grid.

```text
openGrid grid spacing = 28 mm
```

This difference means that accessories using several mounting positions are not directly interchangeable.

For example, over three grid intervals the difference becomes:

```text
3 × 25 mm = 75 mm
3 × 28 mm = 84 mm

difference = 9 mm
```

An adapter may work for an accessory using one mounting point. A wider accessory using several mounting points normally needs to be redesigned for the other grid.

## MultiBoard Connection System

MultiBoard tiles contain two main hole types:

- Small holes
- Larger threaded MultiHoles

The system supports several types of connections, including:

- Snaps
- Weight-bearing snaps
- Threads
- Friction-fit inserts
- Bolt-locked inserts
- Peg-style hooks
- Fix-Points, previously called Multipoints

MultiBoard therefore provides several ways to connect accessories depending on their weight, orientation and intended removability.

Its tiles and related components are based on the wider MultiBuild dimensional system.

## openGrid Connection System

openGrid uses repeated grid openings into which mounting and accessory snaps are inserted.

The board system has two main variants:

```text
Full board = stronger board with greater load capacity
Lite board = thinner board using less filament and printing time
```

Both variants use the same 28 mm spacing.

The Lite board normally includes screw holes for direct mounting.

The Full board commonly uses separate mounting snaps, although generated variants can also include screw holes.

Accessories can be attached using different snap designs, depending on the required direction and locking behaviour.

## Technical Comparison

| Detail | MultiBoard | openGrid |
|---|---|---|
| Grid spacing | 25 mm | 28 mm |
| Base construction | Printed tiles with small holes and threaded MultiHoles | Printed grids with repeated snap openings |
| Connection approach | Multiple snap, thread, insert and peg systems | Primarily snap-based mounting |
| Board variants | Multiple tile and mounting configurations | Full and Lite board variants |
| Direct wall mounting | Several mounting and offset methods | Screw holes or separate mounting snaps |
| Wider ecosystem | Integrated with MultiBin and other MultiBuild components | Independent ecosystem with adapters to other systems |
| Multi-position compatibility | Designed around the 25 mm MultiBuild standard | Designed around the 28 mm openGrid standard |

## MultiBoard Advantages

- Large collection of existing accessories and community designs
- Multiple connection methods for different loads and applications
- Integrated with other MultiBuild systems
- Suitable for tools, bins, shelves, drawers and structural arrangements
- Supports threaded and locking connections
- Uses a consistent 25 mm dimensional standard across the MultiBuild ecosystem

## MultiBoard Disadvantages

- More connector types can make the system harder to understand initially
- A complete installation may require many different small printed parts
- Large surfaces and accessory collections require considerable printing time
- Its licensing and redistribution rules are more restrictive than a conventional open-source licence
- Accessories are tied to the MultiBoard grid and connector geometry

## openGrid Advantages

- Relatively simple base concept centred around a grid and snap interface
- Core system is intended to be openly extendable
- Full and Lite boards allow a choice between strength and material use
- Custom tile generators are available
- Designed for wall, desk and under-desk use
- Adapters and snaps can connect some accessories from other ecosystems
- The openGrid version of Underware can snap directly into the board

## openGrid Disadvantages

- It is a newer ecosystem
- Some categories may have fewer ready-made accessories
- MultiBoard accessories do not automatically fit
- Adapters can add extra parts and mechanical complexity
- Accessories using multiple mounting points must match the 28 mm grid
- Moving from another grid system may require reprinting boards and accessories

## Underware

Underware is a modular cable-management system.

It consists of channels, corners, junctions, holders and other components that can be combined into cable routes.

The original Underware 2.0 release was designed around MultiBoard.

A later openGrid implementation adapts the channels to the openGrid board and attachment geometry.

The relationship is:

```text
same general cable-management concept
different board interface
```

The two versions should therefore not be treated as universally interchangeable parts.

### Underware for MultiBoard

The MultiBoard version uses MultiBoard-compatible connectors to attach cable channels and accessories.

It is useful when a MultiBoard installation already exists or when cable management is combined with the wider MultiBuild ecosystem.

### Underware for openGrid

The openGrid version is redesigned to attach directly to openGrid boards.

The channels can be snapped into the grid without first mounting a separate MultiBoard-style connector.

This may reduce the number of separate connection parts for an openGrid installation.

## Practical Considerations

The forum discussion highlights an important disadvantage shared by both systems: printing a large installation can require substantial time.

The total effort includes more than printing the wall tiles:

- Printing the base boards
- Printing mounting components
- Printing holders and accessories
- Removing supports or cleaning parts
- Assembling small connectors
- Mounting and aligning tiles
- Reprinting parts when the arrangement changes

A small test area may therefore be more useful than immediately printing an entire workshop wall.

## Choosing Between the Systems

MultiBoard may be more suitable when:

- A broad existing accessory ecosystem is important
- Bins, drawers and tool storage are a major requirement
- Integration with MultiBin is useful
- Several connector and locking methods are desirable
- An existing MultiBoard installation is already available

openGrid may be more suitable when:

- A simpler snap-oriented system is preferred
- Open development and modification are important
- Reduced filament use is useful
- Wall, desk and cable organisation are the main applications
- Underware for openGrid is an important intended use
- Custom generated board sizes are required

## Initial Test

Before selecting one system for a large installation, print a small representative test for each.

A useful test could include:

```text
one small board
one wall-mounting method
one simple hook
one heavier holder
one removable accessory
one Underware cable section
```

Compare:

- Printing time
- Filament use
- Ease of assembly
- Connection strength
- Play in the connection
- Ease of repositioning accessories
- Availability of required models
- Ease of designing custom accessories

## Conclusion

MultiBoard and openGrid use the same broad idea: modular printed boards with repositionable accessories.

Their technical implementations are different.

```text
MultiBoard = 25 mm ecosystem with several connection types
openGrid   = 28 mm ecosystem centred around grid snaps
Underware  = cable-management concept available for both systems
```

Neither system is automatically better for every application.

The most practical choice depends on the required accessories, acceptable printing effort, preferred licence model and whether the installation is mainly intended for workshop storage or cable and desk organisation.