Eggetest is a model based exploratory conformance tester. It is
thought to be useful in the testing of systems with concurrent and
combinatorial characteristics.

[1] The model is an Eggenet which is an annotated Petri net formalism.

[2] The model is a closed, folded form and can be unfolded into a
reachability graph (RG). Sometimes RG is called the state space.

[3] The tester interprets the RG against the implementation under test
(IUT). There is an interface definition which describes the stubs
which need to tagged into the IUT. There are four kinds of observable
events in the interface definition: IUT outputs, IUT inputs, crashes,
and hangups.

[4] The tester reports nonconformance between the model and observed
IUT behaviour.

The tester runs for a preset period trying to cover as much
of the RG as possible. It is possible to try and duplicate a previous
run (which, however, is not always feasible since the IUT may be
nondeterminisitic). Previous test runs can be used; earlier RGs can be
used even if the model has changed slightly.

Eggetest uses an ant colony algorithm to find interesting paths to
places where the testing needs to go (e.g. univisited parts of the RG)
and places that the testing has to avoid (example: we only want to run
a crash once and after that we want to avoid the paths leading to the
crash).

Eggetest is the brainchild of Esa Kettunen of Egge Collective, an
inofficial, unregistered collection of individual.

Contact esa.kettunen[at]gmx.com for more information.

Copyright (C) Esa Kettunen 2021