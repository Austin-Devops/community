# New SIG Request
_Please fill out all of the sections below_


#### SIG Proposal Issue
_Link the approved SIG proposal issue here_

#### SIG Pull Request
_Link the SIG PR (as described in the below checklist) here_

#### New SIG Checklist
_Complete the following checklist, indicating completion by ticking the task boxes_
- [ ] Create new IRC channel named `sig-<NEW SIG NAME>`
- [ ] Create and checkout new branch named `sig-<NEW SIG NAME>-new`
  - [ ] Add documentation to new branch in following structure:
      ```
      .
      └── sigs
          ├── OWNERS
          └── <NEW SIG NAME>
              └── README.md     
      ```
      - [ ] `README.md` created from `SIG` `README.md` [template](./README_TEMPLATE/sig_readme_template.md)
      - [ ] `OWNERS` is a yaml file with a single `organizers` that has a value of a list of SIG organizers. These are the people that will have write access to this SIG's documentation. **NOTE**: All writes to the SIG directory require an approved review from an organizer. **YOU CANNOT REVIEW YOUR OWN CODE**. This means that you'll need _at least_ two organizers per SIG.

        ```
        organizers:
          - < ORGANIZER HANDLE > # at least two
        ```

- [ ] Open a new Pull Request from the new `sig-<NEW SIG NAME>` branch against the `master` branch. `@sig-admin` will automatically be added as a reviewer.

#### Finalization
Once the Pull Request has been approved, a member of `@sig-admin` will complete the following:
- [ ] add SIG to the [SIG Master List](../../sigs/sig-master-list.md)
- [ ] create new `@Austin-Devops/sig/sig-<SIG NAME>-organizers` team, populated with the listed SIG organizers       **
   * ensure all organizers are maintainers of this group
- [ ] create new `@Austin-Devops/sig/sig-<SIG NAME>` team, initially populated with the listed SIG organizers        **
   * ensure all organizers are maintainers of this group
- [ ] add `@Austin-Devops/sig-<SIG NAME>-organizers` team as a [Code Owner](../CODEOWNERS) for `/sig/<SIG NAME>/`    **
- [ ] merge PR to `master`


\** _Currently, a repository can only have a single CODEOWNERS file, so these steps must be completed by an admin of this repo. This is okay for the time being, but we need to open an issue to let to find a way to let `sig-admin`s modify the CODEOWNERS file for any directory under /sig/_
___
/cc @sig-admin
