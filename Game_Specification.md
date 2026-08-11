# 📝 Evacuation Protocol - Game Specification (Pre-Alpha)

This document defines the core mechanics for **Phase 1 (Minimum Viable Prototype)** of Evacuation Protocol.

---

## 1. Player Movement & Perspective
The game utilizes a standard, tactical first-person perspective tailored for PC gaming.

*   **Perspective**: Complete First-Person Shooter (FPS) view, synchronized with mouse movement.
*   **Basic Movement**: `W` / `A` / `S` / `D` keys for forward, left, backward, and right navigation.
*   **Sprinting**: Holding down the `Shift` key increases movement speed by 1.5x.
*   **Jumping**: Pressing the `Space` key triggers a jump with natural gravity fall (no cooldown).

---

## 2. Weaponry & Reload Mechanics
The following specifications apply to the baseline weapon for the initial prototype.

*   **Firing**: `Left-Click` to shoot. Supports full-auto firing when held down.
*   **Reloading**: Triggered by pressing the `R` key, or automatically when the magazine reaches 0.
*   **Reload Duration**: **5.0 seconds** (Intentionally long for tactical realism. Firing is disabled during this time).
*   **Magazine Capacity**: **30 rounds** per magazine.

---

## 3. Realistic Ballistics Simulation
*This is the core technical milestone of our project.* We simulate **true physical bullet behavior** instead of simple hitscan.

*   **Projectiles as Entities**: Bullets are generated as independent entities from the muzzle with specific velocity and direction.
*   **Bullet Travel Time**: Projectiles experience actual travel time based on distance, creating a realistic delay before impact.
*   **Bullet Drop (Gravity)**: Projectiles are affected by gravity over time, resulting in a parabolic flight path. Players must aim higher for long-range targets.
*   **Wind Influence**: The architecture should allow for horizontal deviations caused by wind, preparing for the upcoming dynamic weather system.
