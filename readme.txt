The plan is to make a reaper script that humanizes the tempo of the user's project


Assumptions:

    -> Affected area/tracks is/are quantized or acceptably on the grid for user
    -> 

The paramaters:

    What part of timeline to humanize?
        -> selected area (default)
        -> whole project

    What tracks to humanize?
        -> selected tracks (default)
        -> all tracks

    Seed (give option to save seeds)
        -> random (default)
        -> set

    Interval
        -> 1 Bar (defualt)
        -> 2 Bar
        -> 1/2 Note
        -> 1/2 Triplet Note
        -> 1/4 Note
        -> 1/4 Triplet Note
        -> 1/8 Note
        -> 1/8 Triplet Note

    Timing
        -> Sliding scale from 0-100% (default 50%)

Implementation:

    -> Split selected tracks (selected/all) in selected area (selected, whole) at selected intervals
    -> Insert tempo markers at selected intervals
    -> Select items and set timebase to beats (position, length, rate)
    -> Use random seed to add +/- tempo to existing tempo markers with strength timing
    -> Set item timebase back to whatever it was before the transformation
    -> Give user option to glue split tracks back together or keep split by humanized sections
    