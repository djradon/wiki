

## Features

- In case the nested object can be of different types, you can provide an additional options object, that specifies a discriminator. The discriminator option must define a property that holds the subtype name for the object and the possible subTypes that the nested object can converted to. A sub type has a value, that holds the constructor of the Type and the name, that can match with the property of the discriminator.