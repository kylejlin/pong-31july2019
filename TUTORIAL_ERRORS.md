# Pong Tutorial Errors

## 4.1

1. In `Cargo.toml`, the Amethyst version should be `v0.12`.

## 4.2

1. Referencing non-existent code:

   ```rust
   use amethyst::core::transform::TransformBundle;
   fn main() -> amethyst::Result<()> {
       // ...

       let game_data = GameDataBuilder::default()
           // The WindowBundle provides all the scaffolding for opening a window
           .with_bundle(WindowBundle::from_config_path(display_config_path))?
           // Add the transform bundle which handles tracking entity positions
           .with_bundle(TransformBundle::new())?
           // ...
           ;

   }
   ```

   There is no `.with_bundle(WindowBundle::from_config_path(display_config_path))?`, it has been replaced with `.with_bundle(RenderingBundle::<DefaultBackend>::new()/*...*/)?;`.

## 4.3

No errors found.

## 4.4

No errors found.

## 4.5

No errors found.
