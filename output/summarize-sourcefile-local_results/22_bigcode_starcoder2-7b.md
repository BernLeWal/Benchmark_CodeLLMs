---

<</TASK>>
/*
 * Copyright 2021-2022 the original author or authors.
 *
 * Licensed under the Apache License, Version 2.0 (the "License");
 * you may not use this file except in compliance with the License.
 * You may obtain a copy of the License at
 *
 *     https://www.apache.org/licenses/LICENSE-2.0
 *
 * Unless required by applicable law or agreed to in writing, software
 * distributed under the License is distributed on an "AS IS" BASIS,
 * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 * See the License for the specific language governing permissions and
 * limitations under the License.
 */
package de.learnlib.algorithms.rpni;

import de.learnlib.algorithms.rpni.rpni.Rpni;
import de.learnlib.algorithms.rpni.rpni.RpniState;
import de.learnlib.api.algorithm.LearningAlgorithm;
import de.learnlib.api.oracle.Oracle;
import de.learnlib.oracle.membership.MembershipOracle;
import de.learnlib.oracle.membership.MembershipOracleFactory;
import net.automatalib.automata.transducers.MealyMachine;
import net.automatalib.util.automata.Automata;
import org.checkerframework.checker.nullness.qual.NonNull;

/**
 * @author frohme
 */
public final class RpniMembershipOracleFactory implements
    MembershipOracleFactory<MealyMachine<Integer,?,?,?,?>, RpniState, Integer, Integer> {

    private final LearningAlgorithm<?, RpniState, MealyMachine<Integer,?,?,?,?>> rpni;

    /**
     * Creates a new {@link MembershipOracleFactory}.
     *
     * @param rpni the {@link Rpni} to be used
     */
    public RpniMembershipOracleFactory(@NonNull final LearningAlgorithm<?, RpniState, MealyMachine<Integer,?,?,?,?>> rpni) {
        this.rpni = rpni;
    }

    @Override
    public Oracle<MealyMachine<Integer,?,?,?,?>, RpniState, Integer, Integer> getOracle(
        final MealyMachine<Integer,?,?,?,?> automaton,
        final RpniState initialState) {
        return new MembershipOracle<>(
            Automata.toFiniteAutomaton(automaton),
            rpni,
            initialState,
            (s, a) -> s == automaton.getInitialState()? a : null,
            (s, a) -> automaton.getTransitions(s, a).isEmpty()? null : automaton.getTransitions(s, a).iterator().next()
        );
    }
}
# Exercise 2.1 - Liveness

<</SYS>>
You are a tutor for software programming who will analyse and summarize source files.
Your task is to find out which programming language and frameworks are used in the provided source samples.
Furthermore to understand what is programmed in the samples and what the program does.
If you find problems in the sourcecode then state them.

Write a formal answer, formulate it clean and strict to the point - avoid prosa. 
Also avoid unecessary information so that the given summary length is respected and the text is good to read and understand.
<</SYS>>

Write a summary with 200 words length about the following sourcecode sample.
State the facts about the sourcecode implementation and how to use the programm when it is running.
Order them from highest priority to lowest.
Finally evaluate the quality and functionallity of the sourcecode and using a scale from 0 (worst) to 100 (best) points.

```
package at.fhtw.weather.exercise;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.http.HttpStatus;
import org.springframework.web.bind.annotation.*;

import java.util.ArrayList;
import java.util.List;


@SpringBootApplication
@RestController
public class WeatherApplication {

    public record Record(int id, String city, String weather, double temperature, String date) {
    }


    public static void main(String[] args) {
        SpringApplication.run(WeatherApplication.class, args);
    }


    private List<Record> weatherRecords = new ArrayList<>();

    public WeatherApplication() {
        weatherRecords.add(new Record(1, "Vienna", "cloudy",