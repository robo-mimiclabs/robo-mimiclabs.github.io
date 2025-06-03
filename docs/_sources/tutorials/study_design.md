# Design a study

You can use MimicLabs to design a study for your robot policy. Below we describe a few examples.

## Testing compositional generalization

To test combinatorial generalization for placement arrangements, you can design a task suite with the following different object placement arrangements.

Region 1: 
```
(object_init_region
    (:target table)
    (:ranges (
        (-0.2 -0.1 0 0.1)
      )
    )
    (:yaw_rotation (
        (0.0 0.0)
      )
    )
)
```

Region 2:
```
(object_init_region
    (:target table)
    (:ranges (
        (0 0.1 0.2 0.3)
      )
    )
    (:yaw_rotation (
        (0.0 0.0)
      )
    )
)
```

