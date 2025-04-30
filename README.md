### 📋 Full Controller Table (Clean & Complete)

| **Controller**           | **Endpoint**                                     | **Method** | **Action**               | **Description**                                      |
|--------------------------|--------------------------------------------------|------------|---------------------------|------------------------------------------------------|
| **AuthController**       | `/register`                                      | POST       | `register`               | User registration                                    |
|                          | `/login`                                         | POST       | `login`                  | User login                                           |
|                          | `/logout`                                        | POST       | `logout`                 | Logout user                                          |
|                          | `/user`                                          | GET        | `me`                     | Get current user info                                |
|                          | `/auth/google`                                   | GET        | `redirectToGoogle`       | Google OAuth2 redirect                               |
|                          | `/auth/google/callback`                          | GET        | `handleGoogleCallback`   | Handle OAuth2 login callback                         |
| **UserController**       | `/user`                                          | PUT        | `update`                 | Update user profile                                  |
|                          | `/me/properties`                                 | GET        | `myProperties`           | List properties owned by user                        |
|                          | `/me/favorites`                                  | GET        | `favorites`              | List favorite properties                             |
|                          | `/me/favorites/{id}`                             | POST       | `addFavorite`            | Add to favorites                                     |
|                          | `/me/favorites/{id}`                             | DELETE     | `removeFavorite`         | Remove from favorites                                |
| **PropertyController**   | `/properties`                                    | GET        | `index`                  | List all properties                                  |
|                          | `/properties`                                    | POST       | `store`                  | Create a new property                                |
|                          | `/properties/{id}`                               | GET        | `show`                   | Show a single property                               |
|                          | `/properties/{id}`                               | PUT        | `update`                 | Update property details                              |
|                          | `/properties/{id}`                               | DELETE     | `destroy`                | Delete property                                      |
|                          | `/properties/town/{townId}`                      | GET        | `byTown`                 | Properties in a specific town                        |
|                          | `/properties/type/bargains`                      | GET        | `bargains`               | List bargain-type properties                         |
|                          | `/properties/new`                                | GET        | `newListings`            | List newly added properties                          |
|                          | `/properties/recommended`                        | GET        | `recommended`            | Recommended for the user                             |
| **SearchController**     | `/search/properties`                             | GET        | `advancedSearch`         | Full-text + polygon/geo search                       |
| **CityController**       | `/cities`                                        | GET        | `index`                  | List all cities                                      |
|                          | `/cities`                                        | POST       | `store`                  | Create new city                                      |
|                          | `/cities/{id}/towns`                             | GET        | `towns`                  | Get towns within a city                              |
| **TownController**       | `/towns`                                         | POST       | `store`                  | Create new town (polygon)                            |
|                          | `/towns/{id}`                                    | PUT        | `update`                 | Update polygon data                                  |
|                          | `/towns/{id}/properties`                         | GET        | `properties`             | Get properties in a town                             |
| **AnalyticsController**  | `/analytics/global`                              | GET        | `globalAnalytics`        | Market stats across app                              |
|                          | `/analytics/user`                                | GET        | `userAnalytics`          | User-specific stats                                  |
|                          | `/analytics/track-view`                          | POST       | `trackView`              | Log property view                                    |
| **MediaController**      | `/media/upload`                                  | POST       | `upload`                 | Upload image/media                                   |
|                          | `/media/{id}`                                    | DELETE     | `delete`                 | Delete uploaded media                                |
| **AdminController**      | `/admin/users`                                   | GET        | `listUsers`              | List all registered users                            |
|                          | `/admin/properties/pending`                      | GET        | `pendingProperties`      | Get unapproved properties                            |
|                          | `/admin/properties/{id}/approve`                 | POST       | `approveProperty`        | Approve a pending property listing                   |
|                          | `/admin/properties/{id}/reject`                  | DELETE     | `rejectProperty`         | Reject a listing                                     |

---
