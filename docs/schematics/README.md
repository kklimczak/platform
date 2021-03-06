# @ngrx/schematics

Scaffolding library for Angular applications using NgRx libraries.

@ngrx/schematics provides blueprints for generating files when building out feature areas using NgRx. Built on top of `Schematics`, it integrates with the `Angular CLI` to make setting up and expanding NgRx in Angular applications easier.

### Installation

Install @ngrx/schematics from npm:

`npm install @ngrx/schematics --save-dev`

##### OR

`yarn add @ngrx/schematics --dev`

### Nightly builds

`npm install github:ngrx/schematics-builds --save-dev`

##### OR

`yarn add github:ngrx/schematics-builds --dev`

## Dependencies

After installing `@ngrx/schematics`, install the NgRx dependencies.

`npm install @ngrx/{store,effects,entity,store-devtools} --save`

##### OR

`yarn add @ngrx/{store,effects,entity,store-devtools}`

## Default Schematics Collection

To use `@ngrx/schematics` as the default collection in your Angular CLI project,
add it to your `angular.json`:

```sh
ng config cli.defaultCollection @ngrx/schematics
```

The [collection schema](../../modules/schematics/collection.json) also has aliases to the most common blueprints used to generate files.

The `@ngrx/schematics` extend the default `@schematics/angular` collection. If you want to set defaults for schematics such as generating components with scss file, you must change the schematics package name from `@schematics/angular` to `@ngrx/schematics` in `angular.json`:

```json
"schematics": {
  "@ngrx/schematics:component": {
    "styleext": "scss"
  }
}
```

## Initial State Setup

Generate the initial state management and register it within the `app.module.ts`

```sh
ng generate store State --root --module app.module.ts --collection @ngrx/schematics
```

## Initial Effects Setup

Generate the root effects and register it within the `app.module.ts`

```sh
ng generate effect App --root --module app.module.ts --collection @ngrx/schematics
```

## Blueprints

* [Action](action.md)
* [Container](container.md)
* [Effect](effect.md)
* [Entity](entity.md)
* [Feature](feature.md)
* [Reducer](reducer.md)
* [Store](store.md)

## API Documentation

* [Integration with Ionic](ionic.md)
