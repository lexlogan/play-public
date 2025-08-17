.PHONY: test run fmt

test:
	./mvnw -q -DskipITs=false test

run:
	./mvnw -q spring-boot:run

fmt:
	./mvnw -q spotless:apply
