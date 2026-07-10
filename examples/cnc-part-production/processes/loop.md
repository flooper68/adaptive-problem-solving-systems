# CNC production adaptive loop

This example combines planning, execution, compilation, and adaptation in one
small process. A larger implementation may split or parallelize them.

1. Read the approved request, CAD/drawing revision, system strategy, current
   problems with their strategies, task files, relevant prior sessions, compiled
   knowledge, capacity, and constraints.
2. Use current evidence to create or groom one file per open problem under
   `problems/`, with its goal, evidence, desired change, strategy, signal, and
   grooming history. Select batch or investigative work only when its task file
   lists the problem IDs it addresses, then add
   the revision, artifact contract, material, machine, tooling, operations,
   validation, and responsibilities.
3. Resolve load-bearing uncertainty through discussion, research, calculation,
   simulation, coupon testing, or a prototype before committing the batch.
4. Execute the approved setup and toolpath. Update the batch task's current
   state and retain deviations, failed attempts, machine evidence, and
   successful resolutions in native evidence or its session record.
5. Inspect artifact correctness against the released drawing and update the
   conformance problem from the recorded signal. Reject or route nonconformity
   rather than smoothing it over.
6. Send an accepted sample to assembly fit/load validation and update the
   outcome problem from the recorded signal. Record evidence when it arrives;
   artifact completion does not manufacture an outcome.
7. At the locally chosen trigger, review new raw evidence and update
   `knowledge/README.md`; append a short entry to `knowledge/CHANGELOG.md`.
8. Propose changes to strategy, tasks, tooling, execution, validation, or
   system structure. The manufacturing lead approves before the next task uses
   them.
9. Close the batch or schedule the next invocation. Close an open problem only
   under manufacturing-lead authority, recording whether it was solved or
   another closure reason and moving its file under `problems/archive/`; retain
   or reframe it when the signal is unmet.
